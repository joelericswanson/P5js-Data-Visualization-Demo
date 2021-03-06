# P5js-Data-Visualization-Demo

**Required Skills:** a familarity with arrays and for loops

## Given the last year, how do you feel about data-visualization? 

### Reading

[Dietmar Offenhuber, Material Traces as Autographic Visualizations](https://medium.com/multiple-views-visualization-research-explained/material-traces-as-autographic-visualizations-e814662aa60f)

https://www.researchgate.net/publication/344282076_What_We_Talk_About_When_We_Talk_About_Data_Physicality

### Things to Ponder

Data != Fact

>“In order to consider these fundamentals in detail, however, we must start with an alternative assumption about information itself: that there is nothing natural about information. Information, no matter what it is called—data, knowledge, or fact, song, story, or metaphor—has always been designed.” —Brenda Dervin, *Chaos, Order, and Sense-Making* 

["Zero" had to be invented](https://www.scientificamerican.com/article/what-is-the-origin-of-zer/)

[Standards of Measurements have been used as a colonizing tool](https://en.wikipedia.org/wiki/History_of_measurement)

Chart fatigue, New York Times portrait vs. lanscape

[Danielle Szafir](https://danielleszafir.com/), [*The Good, The Bad, and the Biansed: Five Ways Visualization Can Miselad (And How to fix them)*](https://interactions.acm.org/archive/view/july-august-2018/the-good-the-bad-and-the-biased)

## Scales of Measurement

All variables (which compose data) are either *nominal*, *ordinal*, *interval*, and *ratio* as introduced in the 1940's by [Stanley Smith Stevens](https://en.wikipedia.org/wiki/Stanley_Smith_Stevens)

### Qualitative Data 

**Nominal Data: categories, data has no ordering or direction.**
A nominal scale describes a variable with categories that do not have a natural order or ranking. You can code nominal variables with numbers if you want, but the order is arbitrary and any calculations, such as computing a mean, median, or standard deviation, would be meaningless.

Examples: genotype, blood type, zip code, gender, race, eye color, political party (and these many of these categories are social constructions)

**Ordinal Data: ordered categories (ranking, orders or scalings)**

An ordinal scale is one where the order matters but not the difference between values.

Examples: socio economic status (“low income”,”middle income”,”high income”), education level (“high school”,”BS”,”MS”,”PhD”), income level (“less than 50K”, “50K-100K”, “over 100K”), satisfaction rating (“extremely dislike”, “dislike”, “neutral”, “like”, “extremely like”).

Note the differences between adjacent categories do not necessarily have the same meaning. For example, the difference between the two income levels “less than 50K” and “50K-100K” does not have the same meaning as the difference between the two income levels “50K-100K” and “over 100K”.

### Quantitative Data

**Interval Data: Differences between measurements, but no true zero**
An interval scale is one where there is order and the difference between two values is meaningful.

Examples: temperature (Farenheit), temperature (Celcius), pH, SAT score (200-800), credit score (300-850).

**Ratio Data: Differenes between measurements with true zero**
A ratio variable, has all the properties of an interval variable, and also has a clear definition of 0.0. When the variable equals 0.0, there is none of that variable.

Examples: enzyme activity, dose amount, reaction rate, flow rate, concentration, pulse, weight, length, temperature in Kelvin (0.0 Kelvin really does mean “no heat”), survival time.

When working with ratio variables, but not interval variables, the ratio of two measurements has a meaningful interpretation. For example, because weight is a ratio variable, a weight of 4 grams is twice as heavy as a weight of 2 grams. However, a temperature of 10 degrees C should not be considered twice as hot as 5 degrees C. If it were, a conflict would be created because 10 degrees C is 50 degrees F and 5 degrees C is 41 degrees F. Clearly, 50 degrees is not twice 41 degrees.  Another example, a pH of 3 is not twice as acidic as a pH of 6, because pH is not a ratio variable.


### Linear vs. Logarithmic Scales

[Logarithmic Scales](https://en.wikipedia.org/wiki/Logarithmic_scale)

*It is stunning to realize how many people are looking logarithmic data visualizations of Covid and yet have no idea what that means!*


## Tools

* [Python](https://www.python.org/)
* [R](https://www.r-project.org/foundation/)
* [JavaScript](https://www.javascript.com/)
* [Java](https://www.java.com/en/)
* [P5.js](https://p5js.org/)
* [MatLab](https://www.mathworks.com/products/matlab.html)

There are also software packages, like [Tableau](x), that are frequently used.

There are also good tools inside standard software, like Microsoft Excel.

## How do you make a data visualization?

**Start with data!** 
* Find a dataset
* Look at the data. What do you have? What don't you have? 
* Are there other datasets that might be interesting to combine? What story are you trying to tell about this data (in a completely ethical and objective way of course)?
* Start sketching!

## Different Kinds of data

Data is typically stored in an alphanumeric file: .txt file, .csv, .json, etc.

Working with the data format and delivery system is often the most challenging part of visualizing data!

### Raw Text as Data
When dealing with raw text files we need to:
1. Load the text file (make sure it is raw text / .txt)
1. By default a text file is loaded as an *array of lines*, we need to join all the lines together into one string
1. Then we need to separate the big string into into individual strings (words) using *delimeters* (white space and punctuation). You can also do this with a [Regular Expression](https://en.wikipedia.org/wiki/Regular_expression). `/\W+/` will look for all non alphanumeric characters
1. Then we store all the separate words in a new array

[Word Counter](https://editor.p5js.org/hippocrit/sketches/LD2XMdEaG)

[Another Word Counter](https://editor.p5js.org/hippocrit/sketches/qdX42xl7M)

[Letter Counter](https://editor.p5js.org/hippocrit/sketches/4D_Pwiuyf)

*Note: JavaScript p5.js requires a bit of extra work to actually count words. Other programming languages (Python) have built in functionality for this kind of work.*

[Associative Arrays](https://editor.p5js.org/hippocrit/sketches/WzT3mX2Mq)

[Word Frequency](https://editor.p5js.org/hippocrit/sketches/0wqs4QsY9)

[Top Word Counter](https://editor.p5js.org/hippocrit/sketches/urLgOxFmQ)

[Visualize Sentence Length](https://editor.p5js.org/hippocrit/sketches/1t1iGS1q_)

*Note: If you want to work with raw text, use a library like [Rita.js](https://rednoise.org/rita/) if not Python. It will make your life much easier. 

[Parts of Speech](https://editor.p5js.org/hippocrit/sketches/6S4XKdF0EO) 

[Rita Concordance](https://editor.p5js.org/hippocrit/sketches/6S4XKdF0EO)

[More Rita Examples](https://rednoise.org/rita/#examples)

[Even More...][(https://creative-coding.decontextualize.com/intro-to-ritajs/)

### Tables

[CSV: Comma Separated Values](https://en.wikipedia.org/wiki/Comma-separated_values) is like the "lowest common denominator" format for spreadsheets. You might also see the pipe character (|), a colon (:) or a tab, but even if a different delimiter other than a comma is used, they are still called CSV files. (Although sometimes files with tab-separated values are called TSV files.) You can export .CSV files from any spreadsheet software, but keep in mind that you will lose all formatting and data types!

P5.js comes with a bunch of [functions and properties](https://p5js.org/reference/#/p5.Table) for working with tables.

[Load Table](https://editor.p5js.org/hippocrit/sketches/W8-Lt9lby)

[Bar Chart](https://editor.p5js.org/hippocrit/sketches/rQ92oCK8G)

[Line Chart](https://editor.p5js.org/hippocrit/sketches/uNn68IXsP)

[Pie Chart](https://editor.p5js.org/hippocrit/sketches/MteK4lWuF)

*Note: These examples are using imaginary data. You will need to "normalize" your data to make it fit your screen/output. Use the [map()](https://p5js.org/reference/#/p5/map) function to do this.

**Callback Functions**

Instead of using the [preload()](https://p5js.org/reference/#/p5/preload) function, you can write a *callback* function which will be called when the data is loaded. This will give you flexbility, since you may not want to always load data at the beginning of the sketch\.

[Callback Function](https://editor.p5js.org/hippocrit/sketches/xHjCyALEr)

[Loading a Google Spreadsheet](https://editor.p5js.org/hippocrit/sketches/FrqV0s1h0)

[Zip Code Example](https://editor.p5js.org/hippocrit/sketches/WQ0zPLnqc) *This uses [objects](https://p5js.org/examples/objects-objects.html)*

### JSON
The [JSON: JavaScript Object Notation](https://www.json.org/json-en.html) data format is based on the syntax for JavaScript objects, but is widely used on the web.

All JSON data is formatted as an object or an array, both using JavaScript syntax.

A JSON object is identical to a JavaScript object (without functions). It’s a collection of name: value pairs. Note that strings are enclosed in quotes.

```
let animal = {
  "name": "Bambam",
  "breed": "pitbull",
  "age": 9,
  "height": 75,
  "state": "begging"
}

```

An object can contain other objects. Below, the value of “brother” is an object containing two name/value (or key/value) pairs. Also note that the last name/value pair doesn't have a comma after it.

```
{
  "name": "Bambam",
  "breed": "pitbull",
  "age": 9,
  "height": 75,
  "state": "begging",
  "brother":{
    "name":"Smacky",
    "age":3,
    "breed": "boxer"
  }
}
```
When you look at JSON it can look like a mess as whitespace is removed. Copy and paste it into a [JSON Formatter](https://jsonformatter.curiousconcept.com/) to help you understand how the JSON is structured. Working with JSON takes practice. 

[JSON with Array](https://editor.p5js.org/hippocrit/sketches/lIuksZlYi)

[A delightful collection of obscure JSON corpora by Darius Kazemi](https://github.com/dariusk/corpora/tree/master/data)

[External JSON File](https://editor.p5js.org/hippocrit/sketches/mubDkKZj-)

[Loading External JSON File with a Callback Function](https://editor.p5js.org/hippocrit/sketches/MqKnyDuI0)

[Bubble Sort HTML Colors by Hue](https://editor.p5js.org/hippocrit/sketches/Sh5BpMmwE)

### Working with Live Data: API's

So all those previous data sets were static, but how do we work with data that is constantly updating itself, like the weather? This kind of data will typically be served through [API's: Application Programming Interfaces](https://en.wikipedia.org/wiki/API). Getting data from API's can be challenging, as each one is setup slightly differently and you have to learn how work with [QUERY](https://en.wikipedia.org/wiki/Query_string) strings.

[SimpleAPI](https://editor.p5js.org/hippocrit/sketches/vWQm0G6--) **You have to download and run this file due to browser security issues!**

[JSONandAPI](https://editor.p5js.org/hippocrit/sketches/peO1Qe85x)

[APIwithKey](https://editor.p5js.org/hippocrit/sketches/RmB0iiBOO) *You have to sign up (free) to get the API key. Also take a look at the [documentation](https://openweathermap.org/current). This is where you figure out the QUERY string which lets you control the information you get back.*

**Other Examples of Working with API's**

[https://p5js.org/examples/hello-p5-weather.html](https://p5js.org/examples/hello-p5-weather.html)

[https://rebecca-ricks.com/2015/10/27/first-p5-js-sketch-using-the-nyt-api/](https://rebecca-ricks.com/2015/10/27/first-p5-js-sketch-using-the-nyt-api/)

[https://fablab.ruc.dk/introduction-to-using-apis/](https://fablab.ruc.dk/introduction-to-using-apis/)

### Digital Files as Data
Anything digital can be treated as data!

**Sound**

[Microphone Volume](https://editor.p5js.org/hippocrit/sketches/8UVi43Xif)

[Sound Visualizer](https://editor.p5js.org/hippocrit/sketches/u4L8VOCcl)

[Another Sound Visualizer](https://editor.p5js.org/hippocrit/sketches/drODr8Ceg)

**Pixels**

[Read Pixel Data](https://editor.p5js.org/hippocrit/sketches/BFUc32ELr)

[Adjust Video Pixels](https://editor.p5js.org/hippocrit/sketches/_8Lis7eMY)

## Other Links
[List of public API's](https://github.com/public-apis/public-apis/blob/master/README.md)
[Data repository: Kaggle](https://www.kaggle.com/datasets)
[Scatterplot Example by Allison Parrish](https://editor.p5js.org/allison.parrish/sketches/ry9wlx46b)



