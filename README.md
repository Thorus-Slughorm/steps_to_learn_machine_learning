# steps_to_learn_machine_learning
Iam going to learn machine learning and going to share notes also .

First we are going to start learning pandas from W3School  
link : https://www.w3schools.com/python/pandas/default.asp

#There are three things we have to learn :
1. Basics : Introduction , Getting started, Pandas Series , DataFrames , read CSV , read JSON , Analyze Data
2. Cleaning Data , Clean Empty Cells , Clean wrong Format , Clean Wrong Data , Remove Dupliucates
3. Advznced : Correlationn , plotting

#Load a CSV file into a Pandas DataFrame:

 import pandas as pd
 df = pd.read_csv('data.csv')
 print(df.to_string())

#What is Pandas?

1.Pandas is a Python library used for working with data sets.
2.It has functions for analyzing, cleaning, exploring, and manipulating data.

#Why Use Pandas?
 
1.Pandas allows us to analyze big data and make conclusions based on statistical theories.
2.Pandas can clean messy data sets, and make them readable and relevant.
3.Relevant data is very important in data science.

 
#What Can Pandas Do?

Pandas gives you answers about the data. Like:
Is there a correlation between two or more columns?
What is average value?
Max value?
Min value?
Pandas are also able to delete rows that are not relevant, or contains wrong values, like empty or NULL values. This is called cleaning the data.

#Where is the Pandas Codebase?
The source code for Pandas is located at this github repository https://github.com/pandas-dev/pandas

#Some codes > 

import pandas as pd
mydataset = ['BMW','Volvo','Ford'],
'passings':[3,7,2]
}
myvar = pandas.DataFrame(mydataset)
print(myvar)

#What is a Series?
A Pandas Series is like a column in a table.
It is a one-dimensional array holding data of any type.

import pandas as pd
a = [1, 7, 2]
myvar = pd.Series(a)
print(myvar)


#Labels
If nothing else is specified, the values are labeled with their index number. First value has index 0, second value has index 1 etc.

This label can be used to access a specified value

print(myvar[0])
With the index argument, you can name your own labels.

import pandas as pd
a = [1, 7, 2]
myvar = pd.Series(a, index = ["x", "y", "z"])
print(myvar)

Key/value objects as series 
you can also use a key/value object like a dictionary , when creating a series

import pandas as pd
calories = { 'day1' : 420 , 'day2':299 , ; 'day3' : 390}
myvar  = pd.series(calories)
print(myvar)

Now we will create DataFrame from two series :

data = { 'calories':[420,234,223],
          'duration':[30,34,25]
          }
myvar = pd.DataFrame(data)
print(myvar)




