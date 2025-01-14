# excel

# Table of Contents
1. [How to Count all errors in a range](https://github.com/mikeyPower/work_stuff#how-to-count-all-errors-in-a-range)
2. [Count the number of cellignoring errors in a range](https://github.com/mikeyPower/work_stuff#count-the-number-of-cells-ignoring-errors-in-a-range)
3. [Highlight rows based on a certain criteria](https://github.com/mikeyPower/work_stuff#highlight-rows-based-on-a-certain-criteria)
4. [logical operators overview](https://github.com/mikeyPower/work_stuff#excel-logical-operators---overview)
5. [How to use the isblank function](https://github.com/mikeyPower/work_stuff#how-to-use-the-isblank-function)
6. [Logical functions](https://github.com/mikeyPower/work_stuff#excel-logical-functions)
7. [Using AND function](https://github.com/mikeyPower/work_stuff#using-and-function)
8. [Using the OR function](https://github.com/mikeyPower/work_stuff#using-the-or-function)
9. [Using the XOR function](https://github.com/mikeyPower/work_stuff#using-the-xor-function)
10. [Using the NOT function](https://github.com/mikeyPower/work_stuff#using-the-not-function)
11. [Use COUNTA to count cells that arent blank](https://github.com/mikeyPower/work_stuff#use-counta-to-count-cells-that-arent-blank)
12. [Highlight duplicates in a certain range](https://github.com/mikeyPower/work_stuff#find--highlight-duplicates-in-a-certain-range)
13. [Highlight duplicates of a certain-value](https://github.com/mikeyPower/work_stuff#find--highlight-duplicates-of-a-certain-value)
14. [Comparing columns to show unique values](https://github.com/mikeyPower/work_stuff#comparing-columns-to-show-unique-values)
15. [Using VLOOKUP](https://github.com/mikeyPower/work_stuff#using-vlookup)
16. [Count Unique Occurences in Excel](https://github.com/mikeyPower/work_stuff#count-unique-occurences-in-excel)
17. [Select a Range of Cells](https://github.com/mikeyPower/work_stuff#select-a-range-of-cells)
18. [Split Text Strings Into Multiple Columns By Space Comma Delimiter](https://github.com/mikeyPower/work_stuff#split-text-strings-into-multiple-columns-by-space-comma-delimiter)
19. [How to Group Rows](https://github.com/mikeyPower/work_stuff#how-to-group-rows)
20. [Copy visible cells only](https://github.com/mikeyPower/work_stuff#copy-visible-cells-only)
15. [References](https://github.com/mikeyPower/work_stuff#references)

## How to Count all errors in a range

1. In a blank cell, type this formula **=SUM(IF(ISERROR(A1:C10),1))**.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/1.png)

2. Then press **Ctrl+Shift+Enter** keys together, and you will get the number of all the error values of the range.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/2.png)


Note: In the above formula, A1:C10 is the range that you want to use, you can change it as you need.

</br>
## Count The Number Of Specific Types Of Errors In A Range


1. In a blank cell, please type this formula **=COUNTIF(A1:C10,"#DIV/0!")**, see screenshot:

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/doc-count-errors3.png)

2. Then press Enter key, and the number of #DIV/0! error cells will be counted.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/5.png)

Note: In the above formula, A1:C10 is the range that you want to use, and #DIV/0! is the type error that you want to count, you can replace it as your need.


## Count The Number Of Cells Ignoring Errors In A Range

If you want to count the number of cells without errors, you can use this array formula: =SUM(IF( NOT( ISERROR(A1:C10)),1 )), and then press **Ctrl+Shift+Enter** keys simultaneously. And all the cells ignoring error cells will be calculated (including blank cells). See screenshots

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/6.png)

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/7png.png)


## Highlight rows based on a certain criteria

Suppose you have a dataset as shown below and you want to highlight all the records where the Sales Rep name is Bob.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/example-table.png)

Here are the steps to do this:

1. Select the entire dataset (A2:A17 in this example).
2. Click the Home tab.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Home-Tab-in-the-Excel-Ribbon.png)

3. In the Styles group, click on Conditional Formatting.


![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Click-on-Conditional-Formatting.png)

4. Click on ‘New Rules’.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Click-on-New-Rule-Highlight-Rows-Based-on-a-Cell-Value-in-Excel-Conditional-Formatting.png)

5. In the ‘New Formatting Rule’ dialog box, click on ‘Use a formula to determine which cells to format’.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Use-Formula-Option-to-Highlight-Rows-based-on-cell-value.png)

6. In the formula field, enter the following formula: **=$C2=”Bob”**.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Specify-the-Formula-to-Highlight-rows-if-it-is-True.png)

7. Click the ‘Format’ button.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Click-on-the-Format-Button.png)

8. In the dialog box that opens, set the color in which you want the row to get highlighted.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/Color-to-Fill-to-highlight-the-rows.png)

Click OK.

This will highlight all the rows where the name of the Sales Rep is ‘Bob’.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/highlight/All-rows-where-name-is-Bob-are-highlighted.png)

Note that the trick here is to use a dollar sign ($) before the column alphabet ($C1). By doing this, we have locked the column to always be C. So even when cell A2 is being checked for the formula, it will check C2, and when A3 is checked for the condition, it will check C3.

This allows us to highlight the entire row by conditional formatting.


## Excel logical operators - overview


![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20operators/logical%20operators%20overview.PNG)

The screenshot below demonstrates the results returned by Equal to, Not equal to, Greater than and Less than logical operators:

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20operators/excel-logical-operators-example.png)


## Example 1. Using the "Equal to" operator with dates

You might be surprised to know that the Equal to logical operator cannot compare dates as easily as numbers. For example, if the cells A1 and A2 contain the date "12/1/2014", the formula =A1=A2 will return TRUE exactly as it should.

To get the correct result, you must always wrap a date in the DATEVALUE function, like this =A1=DATEVALUE("12/1/2014")

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20operators/equal-to-dates.png)


## Example 2. Using the "Equal to" operator with text values

Using Excel's Equal to operator with text values does not require any extra twists. The only thing you should keep in mind is that the Equal to logical operator in Excel is case-insensitive, meaning that case differences are ignored when comparing text values.

If you want to compare text values taking in to account their case differences, you should use the EXACT function instead of the Equal to operator. The syntax of the EXACT function is as simple as:

    EXACT(text1, text2)
    
Where text 1 and text2 are the values you want to compare. If the values are exactly the same, including case, Excel returns TRUE; otherwise, it returns FALSE.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20operators/equal-to-case-sensitive.png)


## How to use the ISBLANK Function

The Microsoft Excel ISBLANK function can be used to check for blank or null values. The ISBLANK function returns TRUE if the value is blank. The ISBLANK function returns FALSE if the value is not blank.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/isblank/isblank001.gif)

Based on the Excel spreadsheet above, the following ISBLANK examples would return:

    =ISBLANK(A1)
    Result: FALSE

    =ISBLANK(A2)
    Result: TRUE

    =ISBLANK("Tech on the Net")
    Result: FALSE


## Excel Logical Functions

The following table provides a short summary of what each logical function does to help you choose the right formula for a specific task.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/isblank/isblank001.gif)

Excel logical functions - facts and figures
1. In arguments of the logical functions, you can use cell references, numeric and text values, Boolean values, comparison operators, and other Excel functions. However, all arguments must evaluate to the Boolean values of TRUE or FALSE, or references or arrays containing logical values.
2. If an argument of a logical function contains any empty cells, such values are ignored. If all of the arguments are empty cells, the formula returns #VALUE! error.
3. If an argument of a logical function contains numbers, then zero evaluates to FALSE, and all other numbers including negative numbers evaluate to TRUE. For example, if cells A1:A5 contain numbers, the formula =AND(A1:A5) will return TRUE if none of the cells contains 0, FALSE otherwise.
4. A logical function returns the #VALUE! error if none of the arguments evaluate to logical values.
5. A logical function returns the #NAME? error if you've misspell the function's name or attempted to use the function in an earlier Excel version that does not support it. For example, the XOR function can be used in Excel 2016 and 2013 only.


## Using AND function

The AND function tests the conditions you specify and returns TRUE if all of the conditions evaluate to TRUE, FALSE otherwise.

The syntax for the Excel AND function is as follows:

    AND(logical1, [logical2], …)
Where logical is the condition you want to test that can evaluate to either TRUE or FALSE. The first condition (logical1) is required, subsequent conditions are optional.

And now, let's look at some formula examples that demonstrate how to use the AND functions in Excel formulas.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20functions/excel-and-function.png)

One of the most common uses of the Excel AND function is found in the logical_test argument of the IF function to test several conditions instead of just one. For example, you can nest any of the AND functions above inside the IF function and get a result similar to this:

    =IF(AND(A2="Bananas", B2>C2), "Good", "Bad")
    
![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20functions/excel-and-if-functions.png)


## Using the OR function

The difference is that the OR function returns TRUE if at least one if the arguments evaluates to TRUE, and returns FALSE if all arguments are FALSE. The OR function is available in all versions of Excel 2016 - 2000.

The syntax of the Excel OR function is very similar to AND:

    OR(logical1, [logical2], …)
    
And now, let's write down a few formulas for you to get a feel how the OR function in Excel works.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20functions/excel-or-function.png)


As well as Excel AND function, OR is widely used to expand the usefulness of other Excel functions that perform logical tests, e.g. the IF function. Here are just a couple of examples:


    =IF(OR(B2>30, C2>20), "Good", "Bad")

The formula returns "Good" if a number in cell B3 is greater than 30 or the number in C2 is greater than 20, "Bad" otherwise.


## Using the XOR function

The syntax of the XOR function is identical to OR's :

    XOR(logical1, [logical2],…)
The first logical statement (Logical 1) is required, additional logical values are optional. You can test up to 254 conditions in one formula, and these can be logical values, arrays, or references that evaluate to either TRUE or FALSE.

In the simplest version, an XOR formula contains just 2 logical statements and returns:

TRUE if either argument evaluates to TRUE.
FALSE if both arguments are TRUE or neither is TRUE.
This might be easier to understand from the formula examples:

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20functions/excel-xor-function.PNG)


## Using the NOT function

The NOT function is one of the simplest Excel functions in terms of syntax:

NOT(logical)
You use the NOT function in Excel to reverse a value of its argument. In other words, if logical evaluates to FALSE, the NOT function returns TRUE and vice versa. For example, both of the below formulas return FALSE:

    =NOT(TRUE)

    =NOT(2*2=4)
    
For example, when reviewing a list of attire, you may want to exclude some color that does not suit you.  I'm not particularly fond of black, so I go ahead with this formula:

    =NOT(C2="black")
    
![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/logical%20functions/excel-not-function.png)

Translated into plain English, the formula tells Excel to do the following. If the cell C2 is not empty, multiply the number in C2 by 0.15, which gives the 15% bonus to each salesman who has made any extra sales. If C2 is blank, the text "No bonus :(" appears.


## Use COUNTA to count cells that aren't blank

The function counts only the cells that have data, but be aware that "data" can include spaces, which you can't see. And yes, you could probably count the blanks in this example yourself, but imagine doing that in a big workbook. So, to use the formula:

1. Determine the range of cells you want to count. The example above used cells B2 through D6.

2. Select the cell where you want to see the result, the actual count. Let's call that the result cell.

3. In either the result cell or the formula bar, type the formula and press Enter, like so:

        =COUNTA(B2:B6)
        
![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/COUNTA/counta.jpg)


## Find & Highlight Duplicates in a certain range

1. Select the range A1:C10.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/find-duplicates-example.png)

2. On the Home tab, in the Styles group, click Conditional Formatting.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/click-conditional-formatting.png)

3. Click Highlight Cells Rules, Duplicate Values.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/click-highlight-cells-rules-duplicate-values.png)

4. Select a formatting style and click OK

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/select-formatting-style.png)

Result. Excel highlights the duplicate names.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/duplicates.png)


As you can see, Excel highlights duplicates (Juliet, Delta), triplicates (Sierra), quadruplicates (if we have any), etc. Execute the following steps to highlight triplicates only.


## Find & Highlight Duplicates of a certain value

1. Create a new rule.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/new-rule.png)

2. Select 'Use a formula to determine which cells to format'.

3.  Enter the formula **=COUNTIF($A$1:$C$10,A1)=3**.

4. Select a formatting style and click OK.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/new-formatting-rule.png)

Result. Excel highlights the triplicate names.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/duplicates/triplicates.png)

Explanation: =COUNTIF($A$1:$C$10,A1) counts the number of names in the range A1:C10 that are equal to the name in cell A1. If COUNTIF($A$1:$C$10,A1) = 3, Excel formats the cell. Because we selected the range A1:C10 before we clicked on Conditional Formatting, Excel automatically copies the formula to the other cells. Thus, cell A2 contains the formula =COUNTIF($A$1:$C$10,A2)=3, cell A3 =COUNTIF($A$1:$C$10,A3)=3, etc. Notice how we created an absolute reference ($A$1:$C$10) to fix this reference.


## Comparing Columns to show unique values

For example if you want Col C to show entries unique to Col A, and Col D to show entries unique to Col B. These forumlas essentially compares Col A to Col B (and visa versa) and returns there respective unique values.

| A             | B             | C                                         |D
| ------------- |:-------------:|:-----------------------------------------:|-----------------------------------------:|
| 1             | 3             | =IF(ISERROR(MATCH(A1,$B$1:$B$3,0)),A1,"") |=IF(ISERROR(MATCH(B1,$A$1:$A$3,0)),B1,"") |
| 2             | 5             | (fill down)                               |(fill down)                               |
| 3             | 8             | ..                                        |..                                        |



## Using VLOOKUP

1. The VLOOKUP function below looks up the value 53 (first argument) in the leftmost column of the red table (second argument).

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/vlookup/vlookup_overview.PNG)

2. The value 4 (third argument) tells the VLOOKUP function to return the value in the same row from the fourth column of the red table.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/vlookup/vlookup_return.PNG)

Note: the Boolean FALSE (fourth argument) tells the VLOOKUP function to return an exact match. If the VLOOKUP function cannot find the value 53 in the first column, it will return a #N/A error.

The VLOOKUP function always looks up a value in the leftmost column of a table and returns the corresponding value from a column to the right. No worries, you can use the INDEX and the MATCH function in Excel to perform a left lookup.

If the leftmost column of the table contains duplicates, the VLOOKUP function matches the first instance.

The VLOOKUP function in Excel performs a case-insensitive lookup. You can use the INDEX, MATCH and the EXACT function in Excel to perform a case-sensitive lookup.


## Approximate Match

1. The VLOOKUP function below looks up the value 85 (first argument) in the leftmost column of the red table (second argument). There's just one problem. There's no value 85 in the first column.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/vlookup/approx.PNG)

2. Fortunately, the Boolean TRUE (fourth argument) tells the VLOOKUP function to return an approximate match. If the VLOOKUP function cannot find the value 85 in the first column, it will return the largest value smaller than 85. In this example, this will be the value 80.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/vlookup/return_approx.PNG)

3. The value 2 (third argument) tells the VLOOKUP function to return the value in the same row from the second column of the red table.

![alt text](https://github.com/mikeyPower/work_stuff/blob/master/Images%20for%20excel/vlookup/vlookup_return_value.PNG)

Note: always sort the leftmost column of the red table in ascending order if you use the VLOOKUP function in approximate match mode (fourth argument set to TRUE).

## Count Unique Occurences in Excel

The following formula will count the number of unique items in A1:A20000

    =SUMPRODUCT(1/COUNTIF(A1:A20000,A1:A20000))
    
Here were using COUNTIF to count the number of cells in a range that meets a criteria which in this case returns an array of counts of each item in the range.

    =SUMPRODUCT(1/{1;2;1;3;2;1;3;3;....;3;1;5})
 
 ## Select a Range of Cells
 
 In order to select a specified number of cells we can simply enter this into the box that has our current reference A1
 
 ![excel_select](https://user-images.githubusercontent.com/17595044/66813244-54187800-ef2c-11e9-9a48-4708efca5014.PNG)
 
 To select the next 10 rows in Column A simply type A1:A10 into the box and hit enter.
 
 ## Split Text Strings Into Multiple Columns By Space Comma Delimiter
 
 Select the column list you want to split by delimiter, and click Data > Text to Columns. See screenshot:
 
 ![image](https://user-images.githubusercontent.com/17595044/76208885-80dd6c80-61f8-11ea-8ac3-bf9e6be88469.png)
 
 Then a Convert Text to columns Wizard dialog pops out, and check Delimited option, and click Next button. See screenshot:
 
 ![image](https://user-images.githubusercontent.com/17595044/76208924-95ba0000-61f8-11ea-83a4-5c55cb5df795.png)

 In the opening Convert to Text to Columns Wizard - Step 2 of 3 dialog box, please check the delimiter you need to split the data by.
 
 ![image](https://user-images.githubusercontent.com/17595044/76208957-a79ba300-61f8-11ea-8dad-0382416b2e5e.png)
 
 ## How to Group Rows
 
Select one of the larger subsets of data, including all of the intermediate summary rows and their detail rows.
In the dataset below, to group all data for row 9 (East Total), we select rows 2 through 8.

![image](https://user-images.githubusercontent.com/17595044/76209461-d2d2c200-61f9-11ea-984d-22f63b35e312.png)

On the Data tab, in the Outline group, click the Group button, select Rows, and click OK.

![image](https://user-images.githubusercontent.com/17595044/76209504-eb42dc80-61f9-11ea-8905-4edf66cb348e.png)

This will add a bar on the left side of the worksheet that spans the selected rows:

![image](https://user-images.githubusercontent.com/17595044/76209523-fb5abc00-61f9-11ea-8504-4fd60acd0362.png)

In a similar manner, you create as many outer groups as necessary.

## Copy visible cells only

Select the cells that you want to copy

Click Home > Find & Select, and pick Go To Special.

![image](https://user-images.githubusercontent.com/17595044/76212012-6c50a280-61ff-11ea-8825-3c88c5af7a7c.png)

Click Visible cells only > OK.

![image](https://user-images.githubusercontent.com/17595044/76212121-a9b53000-61ff-11ea-931e-e85e58a6e20b.png)

Click Copy (or press Ctrl+C).

![image](https://user-images.githubusercontent.com/17595044/76212046-85f1ea00-61ff-11ea-90ab-de443f0f02cd.png)

Select the upper-left cell of the paste area and click Paste (or press Ctrl+V).
    
## References


1. [Exceljet](https://exceljet.net/)
2. [Ablebits](https://www.ablebits.com/)
3. [stackoverflow](https://stackoverflow.com/)
4. [Microsoft Support](https://support.office.com/)
