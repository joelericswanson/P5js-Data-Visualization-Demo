# P5js-Data-Visualization-Demo
### Required Skills
a familarity with arrays and for loops

### Things to Ponder: Data != Truth
>“In order to consider these fundamentals in detail, however, we must start with an alternative assumption about information itself: that there is nothing natural about information. Information, no matter what it is called—data, knowledge, or fact, song, story, or metaphor—has always been designed.” —Brenda Dervin, *Chaos, Order, and Sense-Making* 

["Zero" had to be invented](https://www.scientificamerican.com/article/what-is-the-origin-of-zer/)

[Standards of Measurements have been used as a colonizing tool](https://en.wikipedia.org/wiki/History_of_measurement)

Chart fatigue, New York Times portrait vs. lanscape

[Danielle Szafir](https://danielleszafir.com/), [*The Good, The Bad, and the Biansed: Five Ways Visualization Can Miselad (And How to fix them)*](https://interactions.acm.org/archive/view/july-august-2018/the-good-the-bad-and-the-biased)

## Scales of Measurement

All variables (which compose data) are either nominal, ordinal, interval, and ratio as introduced in the 1940's by [Stanley Smith Stevens](https://en.wikipedia.org/wiki/Stanley_Smith_Stevens)

![Types of Data](https://lh5.googleusercontent.com/7jyxzQ2ObysJGLFcGB6Zc25AHAswexk68SbOh_KYa4if2P9yRe7lIC8NDUgZEcSGspqpRIGQcMx_qCmrG6sjHegFHy9Sqhp_1z3PFido6d19TKYFq0pMTHDs4OV9l6pP-MTNmeKu)

### Qualitative Data 

**Nominal Data: categories, data has no ordering or direction.**
A nominal scale describes a variable with categories that do not have a natural order or ranking. You can code nominal variables with numbers if you want, but the order is arbitrary and any calculations, such as computing a mean, median, or standard deviation, would be meaningless.

Examples: genotype, blood type, zip code, gender, race, eye color, political party

**Ordinal Data: ordered categories (ranking, orders or scalings)**

An ordinal scale is one where the order matters but not the difference between values.

Examples: socio economic status (“low income”,”middle income”,”high income”), education level (“high school”,”BS”,”MS”,”PhD”), income level (“less than 50K”, “50K-100K”, “over 100K”), satisfaction rating (“extremely dislike”, “dislike”, “neutral”, “like”, “extremely like”).

Note the differences between adjacent categories do not necessarily have the same meaning. For example, the difference between the two income levels “less than 50K” and “50K-100K” does not have the same meaning as the difference between the two income levels “50K-100K” and “over 100K”.

### Quantitative Data

**Interval Data: Differences between measurements, but no true zero**
An interval scale is one where there is order and the difference between two values is meaningful.

Examples temperature (Farenheit), temperature (Celcius), pH, SAT score (200-800), credit score (300-850).

**Ratio Data: Differenes between measurements with true zero**
A ratio variable, has all the properties of an interval variable, and also has a clear definition of 0.0. When the variable equals 0.0, there is none of that variable.

Examples: enzyme activity, dose amount, reaction rate, flow rate, concentration, pulse, weight, length, temperature in Kelvin (0.0 Kelvin really does mean “no heat”), survival time.

When working with ratio variables, but not interval variables, the ratio of two measurements has a meaningful interpretation. For example, because weight is a ratio variable, a weight of 4 grams is twice as heavy as a weight of 2 grams. However, a temperature of 10 degrees C should not be considered twice as hot as 5 degrees C. If it were, a conflict would be created because 10 degrees C is 50 degrees F and 5 degrees C is 41 degrees F. Clearly, 50 degrees is not twice 41 degrees.  Another example, a pH of 3 is not twice as acidic as a pH of 6, because pH is not a ratio variable.


### Linear vs. Logarithmic Scales

[Logarithmic Scales](https://en.wikipedia.org/wiki/Logarithmic_scale)

*It is stunning to realize how many people are looking logarithmic data visualizations of Covid and yet have no idea what that means!*


## Tools
[Python](https://www.python.org/)
[R](https://www.r-project.org/foundation/)
[JavaScript](https://www.javascript.com/)
[Java](https://www.java.com/en/)
[P5.js](https://p5js.org/)
[MatLab](https://www.mathworks.com/products/matlab.html)

There are also software packages, like [Tableau](x), that are frequently used.

There are also good tools inside standard software, like Microsoft Excel.

## How do you make a data visualization?

**Start with data!** Look at the data. What do you have? What do you not have? Is there other data that might be interesting to combine? What story are you trying to tell about this data (in a completely ethical and objective way of course)?

Start sketching!

## Different Kinds of data

Data usually comes formatted as some kind of text: .txt file, .csv, .json, etc.

Working with the data format and delivery system is often the most challenging part of visualizing data!

### Raw Text as Data
When dealing with raw text files we need to:
1. Load the text file (make sure it is raw text / .txt)
1. By default text file is loaded as an *array of lines*, we need to join all the lines together into one string
1. Then we need to separate the big string into into individual strings (words) using *delimeters* (white space and punctuation)
1. Then we store all the separate words in a new array

[Word Counter](https://editor.p5js.org/hippocrit/sketches/LD2XMdEaG)

[Letter Counter](https://editor.p5js.org/hippocrit/sketches/4D_Pwiuyf)

*Note: JavaScript p5.js requires a bit of extra work to actually count words. Other programming languages (Python) have built in functionality for this kind of work.*

[Associative Arrays](https://editor.p5js.org/hippocrit/sketches/WzT3mX2Mq)

[Word Frequency](https://editor.p5js.org/hippocrit/sketches/0wqs4QsY9)

[Top Word Counter](https://editor.p5js.org/hippocrit/sketches/urLgOxFmQ)

*Note: If you want to work with raw text, use a library like [Rita.js](https://rednoise.org/rita/). It will make your life much easier.

### Tables

[CSV: Comma Separated Values](https://en.wikipedia.org/wiki/Comma-separated_values)

CSV is the lowest level standard for spreadsheets. You might also see the pipe character (|), a colon (:) or a tab. But even if a different delimiter other than a comma is used, such files are still called CSV files. (Although sometimes files with tab-separated values are called TSV files.)

You can export .CSV files from any spreadsheet software, but keep in mind that you will lose all formatting and data types!

P5.js comes with a bunch of [functions and properties](https://p5js.org/reference/#/p5.Table) for working with tables.

[Load Table](https://editor.p5js.org/hippocrit/sketches/W8-Lt9lby)
[Bar Chart](https://editor.p5js.org/hippocrit/sketches/rQ92oCK8G)
[Line Chart](https://editor.p5js.org/hippocrit/sketches/uNn68IXsP)
[Pie Chart](https://editor.p5js.org/hippocrit/sketches/MteK4lWuF)
*Note: These examples are using imaginary data. You will need to "normalize" your data to make it fit your screen/output. Use the [map()](https://p5js.org/reference/#/p5/map) function to do this.

**Callback Functions**

Instead of using the `[preload()](https://p5js.org/reference/#/p5/preload)` function you can write a `callback` function which will be called when the data is loaded. This will give you flexbility, since you may not want to always load data at the beginning of the sketch\.

[Callback Function](https://editor.p5js.org/hippocrit/sketches/xHjCyALEr)

[Loading a Google Spreadsheets](https://editor.p5js.org/hippocrit/sketches/FrqV0s1h0)

[Zip Code Example](https://editor.p5js.org/hippocrit/sketches/WQ0zPLnqc) *This uses objects*

### JSON
[JSON: JavaScript Object Notation](https://www.json.org/json-en.html)

`{
  		"name":"cat",
  		"weight": 11,
  		"breed": "Siamese",
  		"eyecolor": "blue"  
}`

Check your formatting: [https://jsonformatter.curiousconcept.com/](https://jsonformatter.curiousconcept.com/)

[JSON with Array](https://editor.p5js.org/hippocrit/sketches/lIuksZlYi)

Note: JSON is great, but the trick is getting used to "traversing," or getting the right syntax to get the data you want. 

[A delightful collection of obscure JSON corpora by Darius Kazemi](https://github.com/dariusk/corpora/tree/master/data)

[External JSON File](https://editor.p5js.org/hippocrit/sketches/mubDkKZj-)
[Loading External JSON File with a Callback Function](https://editor.p5js.org/hippocrit/sketches/MqKnyDuI0)

[Bubble Sort HTML Colors by Hue](https://editor.p5js.org/hippocrit/sketches/Sh5BpMmwE)
*Something I've been working on recently (using a Bubble Sort Algorithm to resort an alphabetized list of the named HTML colors based on Hue.*

### Working with Live Data: API's

All the previous data was static: it doesn't update itself. But how do we work with data this is constantly updating itself, like weather? Most of this kind of data will be served through API's: Application Programming Interfaces. Getting data from API's can be challenging, as each one is setup slightly differently and you have to learn how to access their data through QUERYs.

Let's start with a very simple example of an API: [http://api.open-notify.org/astros.json](http://api.open-notify.org/astros.json)

[Weather API](https://editor.p5js.org/hippocrit/sketches/RmB0iiBOO)

Notice: 
*We request the data right through the browser via `http://`
*This API doesn't require any kind of authentication. Most of them do.
*The data is returned as a JSON file



[List of public API's](https://github.com/public-apis/public-apis/blob/master/README.md)

Other Examples of Working with API's
https://p5js.org/examples/hello-p5-weather.html
https://rebecca-ricks.com/2015/10/27/first-p5-js-sketch-using-the-nyt-api/
[Daniel Shiffman's API Tutorial](https://shiffman.net/a2z/data-apis/)
https://fablab.ruc.dk/introduction-to-using-apis/

### Digital Files as Data
Anything digital can be treated as data!

Sound
https://www.creativebloq.com/how-to/data-visualisation-with-p5js

Pixel

Data repository: [Kaggle](https://www.kaggle.com/datasets)


Not really a "type of data" but you will often get data through an [API: Application Programming Interface](https://en.wikipedia.org/wiki/API). Most API's deliver JSON formatted data.

##Query Strings



Other great Examples
[Scatterplot Example by Allison Parrish](https://editor.p5js.org/allison.parrish/sketches/ry9wlx46b)

