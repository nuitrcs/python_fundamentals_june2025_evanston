# Exercise – Conversion Calculator

## Goal

In today's exercise, you will write Python code that converts a given value from its original unit to a different unit.

You will use the data file, `conversionMeasures.csv`, which contains lines of data.  Each line in the file has three pieces of data separated by commas: `from_unit,conversion_factor,to_unit`.  

For example, below are the first few lines of the file:

```
kilometer,1000,meter
meter,100,centimeter
inch,2.54,centimeter
```

Your code will use this information to convert a value from one unit to another.

The conversion equation for all of these lines is
```
from_unit x conversion_factor = to_unit
```

Your code should be able to convert the following test cases:

```
from_unit = "pint"
test_value = 2.5
to_unit = "mL"

from_unit = "cubic_foot"
test_value = 30
to_unit = "liter"

from_unit = "slug"
test_value = "4.8" # Yes, you should write your code to handle values that are entered as strings
to_unit = "pound"

from_unit = "slug"
test_value = 27.0
to_unit = "snail" # See 'Errors to anticipate' below
```

By the end of day, your code should:

- Read the conversion data from the `conversionMeasures.csv` file and store it as a data structure in a python object (list of lists, dictionary of dictionaries, etc.)
- Find the correct conversion factor for a given unit from your python object containing the data
- Include a function to convert between units
- Print out a full sentence response with the final answer
- Anticipate some errors (more on this below)
- Run your code on the provided test examples

## Getting Started

You will first need to make a new notebook in Jupyter or Colab that runs Python 3.

Within the notebook, the first step will be to read in the data from the csv file.

If you are using a Colab notebook, you will need to run a cell at the top of your notebook that says:

```
!wget https://raw.githubusercontent.com/nuitrcs/python_workshops_datarepo/refs/heads/main/conversionMeasures.csv
```

This line loads the data stored in our GitHub repo into your Google Colab workspace.

If you work in a Jupyter notebook (running on your computer), you can either use the same `wget` command above, or manually download the file from this GitHub repo, and then point your code to the file location on your computer.



## Errors to anticipate

Here are two errors that you should anticipate and check for.

1.	Someone might give the initial value as a string instead of a float or integer.
2.	Someone might request a unit that is not in your data – your code should print out an error message. Here’s a sample to test for this error.  (Unit "snail" does not exist.):

```
test_unit = "slug"
test_value = 27.0
final_unit = "snail"
```
(Feel free to think of and check for other potential errors as you write your code and review the data file.)

## Tips

* You may benefit from writing out the steps you need to complete each task before you start coding
* Take it one step at a time
* If you are stuck you can look at the [part5-extraHelp.md](part5-extraHelp.md) document that contains additional tips (but please try yourself before peeking!)

## Python notebook and script organization

While you can get the above done in a chaotic manner, we want you to try some best practices when creating python notebooks. Following best practices, endeavor to organize your notebook in the following order:

1. A description of what the notebook or script does, what type of data you must or can use (file type, required columns, etc.), and what products (files, visualizations, reports, etc.) are made. (While this appears first in a finalized notebook, it is usually prepared or finalized last, once you have a better idea of how other sections fit together).
2. Import any packages used
3. Define any input or output filenames, saving the file paths as variables
4. Loading of data, cleaning of data, and creation of data structures that will be used throughout the code (dictionaries, lists, etc.)
5. Define any custom functions or objects that will be used in the body of the code
6. Body of the code (calling functions, looping, cleaning data, doing calculations, etc.)

## BONUS CHALLENGES

1.	Someone might give a test or final unit that has different capitalization than how it is presented in the csv file. Edit your code so that it can still process this sample:

```
test_unit = "KM/H"
test_value = 8.4
final_unit = m/Sec
```

2. Someone might give a unit that has spaces instead of the underscores that are in your data csv file.  Edit your code so that it can still process this sample:

```
from_unit = "cubic foot"
test_value = 30
to_unit = "liter"
```

3.	In the csv file, not all the units are included on both sides of the conversion factor. Someone might give you a unit from the right side of the factor and ask you to convert it to the unit on the left side, which would require division instead of multiplication. Edit your code so that it can process this sample:

```
test_unit = "ergs"
test_value = 8.4
final_unit = "joule"
```

4.	Advanced Challenge: there's a function called `input()` that can collect data from the user of your code in real time. Here's a link to a website that describes the `input()` function: https://www.w3schools.com/python/ref_func_input.asp. Try to use the `input()` function to collect the `from_unit`, `test_value`, and `to_unit` values.
