![Project logo](https://github.com/Tw1ddle/MarkovNameGenerator/blob/master/screenshots/markovnamegen_logo.png?raw=true "Project logo")

WORK IN PROGRESS

Markov process name generator. Demonstrates usage of the Haxe [markov-namegen haxelib](http://lib.haxe.org/p/markov-namegen).

## Features ##
* Interactively configure the training dataset, order and prior parameters.
* Filter results by length, start, end and content.
* Sort results by their Damarau-Levenshtein similarity to your preferred result.
* Smart trie visualization of the training dataset and generated names.

## Usage ##

Open the [demo](http://www.samcodes.co.uk/web/markov-name-generator/) in your browser to see what the library is capable of. Example settings:

```
Training Dataset: English Towns
Order: 5
Prior: 0.01
Max Processing Time: 500ms
Length: 8-11
Starts with: b
Ends with:
Include: ham
Exclude:
Similarity To: "birmingham"
```

A list of up to 100 results will be returned. Here are the top 10 from my attempt:
```
Barkingham
Basingham
Birkenham
Bebingham
Bollingham
Bridlingham
Billenham
Berwickham
Botteringham
Bradnincham
```

## Install ##

Get the Haxe library code here or on haxelib. 

Include it in your ```.hxml```
```
-lib markovnamegen
```

Or add it to your ```Project.xml```:
```
<haxelib name="markovnamegen" />
```

## Screenshots ##
Here is the demo in action:

![Screenshot](https://github.com/Tw1ddle/MarkovNameGenerator/blob/master/screenshots/screenshot1.png?raw=true "Screenshot 1")

## Notes ##
* Most of the concepts used for the generator were suggested in [this article](http://www.roguebasin.com/index.php?title=Names_from_a_high_order_Markov_Process_and_a_simplified_Katz_back-off_scheme) by [Jeffrey Lund](https://github.com/jlund3).
* The internal state of the generator is visualized using [d3.js](http://d3js.org/).
* The haxelib should function on every Haxe target, but it has not been tested or optimized for performance, especially on native platforms.