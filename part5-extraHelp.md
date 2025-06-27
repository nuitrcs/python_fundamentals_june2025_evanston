# If you need extra help...


You may find it helpful to divide your code into the following three sections:

## Section 1

Read `conversionMeasures.csv` and store the information as a Python data object. There are multiple options for data types (list of lists, list of dictionaries, dictionary of dictionaries, etc.) depending on how you aim to find the conversion in Section 2.  Here is an example workflow to create a list of lists
- Open the file in read mode (e.g., using a `with` statement).
- Save as a list of lines with `f.readlines()`.
- Exit the `with` statement.
- Create an empty list.
- Loop through the lines from the file.
- For each line, remove the trailing new line character and split the line on the commas, which will make a list.
- Append the list to the empty list you made above.
- After completing the loop, you should have a list of lists.

## Section 2

Given an input `from_unit` and an input `to_unit` (e.g., from the provided test cases), identify the correct conversion factor using the data object created in Section 1. After identifying the conversion factor, convert the unit using the formula.  Here is an example workflow using a list of lists:
- Create a function to identify the conversion factor and then convert between units.
    - The function should take the conversion data object (i.e., the list of lists), the desired `from_unit` and `to_unit`, and the desired value to convert as input arguments.
    - First, the function should loop through your list of lists conversion object.
    - Within the loop, check if the input `from_unit` is equal to the item in the first position of the list and if the input `to_unit` is equal to the third item in the list.  If so, save the second item in the list and break the loop.  (This second item is the conversion factor.)
    - Next the function should perform the conversion, and return the resulting value.
- Call your function with each of the test cases.

## Section 3

Finalize and clean up the code. 
- Print out a full sentence response with the final answer for each test case. 
- Include checks within your code for the possible errors we specified (and more if desired).  Verify that these checks catch the errors.  Provide helpful output for the user if the code catches an error. 
- Add documentation (e.g., comments and/or docstrings) so that others can more easily understand your code
- Consider consolidating and cleaning up any components of your code that were not written well enough or are no longer needed.

