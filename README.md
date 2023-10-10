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

 
<< :: #What Can Pandas Do?

Pandas gives you answers about the data. Like:
Is there a correlation between two or more columns?
What is average value?
Max value?
Min value?
Pandas are also able to delete rows that are not relevant, or contains wrong values, like empty or NULL values. This is called cleaning the data.

#Where is the Pandas Codebase?
The source code for Pandas is located at this github repository https://github.com/pandas-dev/pandas

<< :: #Some codes > 

import pandas as pd
mydataset = ['BMW','Volvo','Ford'],
'passings':[3,7,2]
}
myvar = pandas.DataFrame(mydataset)
print(myvar)

<< :: #What is a Series?
A Pandas Series is like a column in a table.
It is a one-dimensional array holding data of any type.

import pandas as pd
a = [1, 7, 2]
myvar = pd.Series(a)
print(myvar)


#Labels
If nothing else is specified, the values are labeled with their index number. First value has index 0, second value has index 1 etc.

<< :: This label can be used to access a specified value

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

<< :: Now we will create DataFrame from two series :

data = { 'calories':[420,234,223],
          'duration':[30,34,25]
          }
myvar = pd.DataFrame(data)
print(myvar)

<< :: ##Now lets talk about Pandas dataframe :: >>

What is a DataFrame ?
A Pandas DataFrame is a 2 dimensional data structure, like a 2 dimensional array, or a table with rows and columns.
Example

import pandas as pd
data={'calories':[454,353,355],'duration':[90,45,34] }
#now going to load the data into dataframe object
df = pd.DataFrame(data)
print(df)

Result

     calories  duration
  0       420        50
  1       380        40
  2       390        45


<< :: Locate Row :: >>
As you can see from the result above, the DataFrame is like a table with rows and columns.
Pandas use the loc attribute to return one or more specified rows.

print(df.loc[0])
Result

  calories    420
  duration     50
  Name: 0, dtype: int64
<<:: Return row 0 and 1:

#use a list of indexes:
print(df.loc[[0, 1]])


     calories  duration
  0       420        50
  1       380        40

<< :: Now named indexes :: >>
With the index argument , you can name your own indexes ..

import pandas as pd
data={"calories":[343,344,345],'duration':[34,55,43]}
df = DataFrame(data,index = ['day1','day2','day3'])
print(df)

Result

        calories  duration
  day1       420        50
  day2       380        40
  day3       390        45

  
<<::>> Locate Named Indexes <<::>>
Use the named index in the loc attribute to return the specified row(s).

Example
Return "day2":

#refer to the named index:
print(df.loc["day2"])

  Result

  calories    380
  duration     40
  Name: day2, dtype: int64
  
<<::*::>>

After this all basics now we arre going to 
Load Files Into a DataFrame
If your data sets are stored in a file, Pandas can load them into a DataFrame.

Example
Load a comma separated file (CSV file) into a DataFrame:

import pandas as pd
df = pd.read_csv('data.csv')
print(df) 

now we are going to load the csv into dataframe ::>>
import pandas as pd
df = pd.read_csv('data.csv')
print(df.to_string())

Tip::>> use to_string() to print the entire DataFrame.
<<::*::>>
 [*] max_rows [*]
The number of rows returned is defined in Pandas option settings.
You can check your system's maximum rows with the pd.options.display.max_rows statement.
Example
Check the number of maximum returned rows:

import pandas as pd
print(pd.options.display.max_rows) 

60
In my system the number is 60, which means that if the DataFrame contains more than 60 rows, the print(df) statement will return only the headers and the first and last 5 rows.

You can change the maximum rows number with the same statement.

Example
Increase the maximum number of rows to display the entire DataFrame:

import pandas as pd
pd.options.display.max_rows = 9999
df = pd.read_csv('data.csv')
print(df)

<<::::>>
Pandas Read JSON
<<::::>>
Read JSON
Big data sets are often stored, or extracted as JSON.
JSON is plain text, but has the format of an object, and is well known in the world of programming, including Pandas.

import pandas as pd
df=pd.read_json('data.json')
print(df.to_string())

<<::Dictionary as JSON::>>
JSON = Python Dictionary 
JSON objects have the same format as Python dictionaries.

import pandas as pd
data = { "duration":{"0":60,
"1":50,
"2":23,
"3":45,
"4":117,
"5":102
  },
  "Maxpulse":{
    "0":130,
    "1":145,
    "2":135,
    "3":175,
    "4":148,
    "5":127
  },
  "Calories":{
    "0":409,
    "1":479,
    "2":340,
    "3":282,
    "4":406,
    "5":300
  }
}
df = pd.DataFrame(data)
print(df)

<<::::>> <<::::>> <<::::>>

**Pandas - Analyzing DatFrames**
Viewing the Data
One of the most used method for getting a quick overview of the DataFrame, is the head() method.The head() method returns the headers and a specified number of rows, starting from the top.

ExampleGet your own Python Server
Get a quick overview by printing the first 10 rows of the DataFrame:

import pandas as pd

df = pd.read_csv('data.csv')

print(df.head(10))
 and if we use only head() it will give us only top 5 items ::>>
and for the last 5 rows 
we use tail()

print(df.tail())
<<::>>
<<::>>
#info about the data
df.info()

<<::::>> <<::::>> <<::::>>

<<##>> Data Cleaning <<##>>

<<::::>> <<::::>> <<::::>>
Data Cleaning
Data cleaning means fixing bad data in your data set.

Bad data could be:

Empty cells
Data in wrong format
Wrong data
Duplicates

we are going to deal with these problems ::
Our Data Set
In the next chapters we will use this data set:


      Duration          Date  Pulse  Maxpulse  Calories
  0         60  '2020/12/01'    110       130     409.1
  1         60  '2020/12/02'    117       145     479.0
  2         60  '2020/12/03'    103       135     340.0
  3         45  '2020/12/04'    109       175     282.4
  4         45  '2020/12/05'    117       148     406.0
  5         60  '2020/12/06'    102       127     300.0
  6         60  '2020/12/07'    110       136     374.0
  7        450  '2020/12/08'    104       134     253.3
  8         30  '2020/12/09'    109       133     195.1
  9         60  '2020/12/10'     98       124     269.0
  10        60  '2020/12/11'    103       147     329.3
  11        60  '2020/12/12'    100       120     250.7
  12        60  '2020/12/12'    100       120     250.7
  13        60  '2020/12/13'    106       128     345.3
  14        60  '2020/12/14'    104       132     379.3
  15        60  '2020/12/15'     98       123     275.0
  16        60  '2020/12/16'     98       120     215.2
  17        60  '2020/12/17'    100       120     300.0
  18        45  '2020/12/18'     90       112       NaN
  19        60  '2020/12/19'    103       123     323.0
  20        45  '2020/12/20'     97       125     243.0
  21        60  '2020/12/21'    108       131     364.2
  22        45           NaN    100       119     282.0
  23        60  '2020/12/23'    130       101     300.0
  24        45  '2020/12/24'    105       132     246.0
  25        60  '2020/12/25'    102       126     334.5
  26        60    2020/12/26    100       120     250.0
  27        60  '2020/12/27'     92       118     241.0
  28        60  '2020/12/28'    103       132       NaN
  29        60  '2020/12/29'    100       132     280.0
  30        60  '2020/12/30'    102       129     380.3
  31        60  '2020/12/31'     92       115     243.0

The data set contains some empty cells ("Date" in row 22, and "Calories" in row 18 and 28).

The data set contains wrong format ("Date" in row 26).

The data set contains wrong data ("Duration" in row 7).

The data set contains duplicates (row 11 and 12).


<<::::>> Now we are going to clean empty cells ::>>
>> by removing rows
>> import pandas as pd
>> df = pd.read_csv("data.csv")
>> new_df = df.dropna()
>> print(new_df.to_string())

By default, the dropna() method returns a new DataFrame, and will not change the original.
 <<::::>>
 <<::::>>
Remove all rows with NULL values:

import pandas as pd
df = pd.read_csv('data.csv')
df.dropna(inplace = True)
print(df.to_string())

Now, the dropna(inplace = True) will NOT return a new DataFrame,
but it will remove all rows containing NULL values from the original DataFrame.
<<:::>>
<<::>>
Replace Empty Values
Another way of dealing with empty cells is to insert a new value instead.
This way you do not have to delete entire rows just because of some empty cells.
The fillna() method allows us to replace empty cells with a value:

Example
Replace NULL values with the number 130:

import pandas as pd
df = pd.read_csv('data.csv')
df.fillna(130, inplace = True)

<<::::>>
Replace Using Mean, Median, or Mode 
<<::::>>

A common way to replace empty cells, is to calculate the mean, median or mode value of the column.
Pandas uses the mean() median() and mode() methods to calculate the respective values for a specified column:

Example
Calculate the MEAN, and replace any empty values with it:

import pandas as pd
df = pd.read_csv('data.csv')
x = df["Calories"].mean()
df["Calories"].fillna(x, inplace =True)

<<Mean = the average value (the sum of all values divided by number of values)>>

Calculate the MEDIAN, and replace any empty values with it:

import pandas as pd
df = pd.read_csv('data.csv')
x = df["Calories"].median()
df["Calories"].fillna(x, inplace = True)

>> Median = the value in the middle, after you have sorted all values ascending.
>> Calculate MODE :
>> import pandas as pd
>> x = df["Calories"].mode()[0]
>> df["Calories:].fillna(x, inplace = true)
>> Mode = the value that appears most frequently.

## Pandas - Cleaning Data of Wrong Format
>> Convert Into a Correct Format
Convert to date ::>>
>>
>> import pandas as pd
>> df = pd.read_csv(data.csv")
>> df['Date'] = pd.to_datetime(df['Date'])
>> print(df.to_string())
>> this will mae it in the right format only for dates null
>> will remain null 

Removing Rows ::>> Remove rows with a NULL value in the "Date" column:
df.dropna(subset=['Date'],inplace = True)

<<:: ::>>
Wrong Data :: >>
removing rows , changing values  , discovering duplicates ,
Pandas - Fixing Wrong Data
>> print(df.duplicated())
>> Removing Duplicates
To remove duplicates, use the
>> drop_duplicates()   method.
>> df.drop_duplicates(inplace = True)
>>
>> The (inplace = True) will make sure that the method does NOT return a new DataFrame, but it will remove all duplicates from the original DataFrame.

<<:: ::>> <<:: ::>>
Pandas - Data Correlations :: >>
Finding Relationships ::>>
A great aspect of the Pandas module is the corr() method.
The corr() method calculates the relationship between each column in your data set.
The examples in this page uses a CSV file called: 'data.csv'.
>> df.corr()
>> 
            Duration     Pulse  Maxpulse  Calories
  Duration  1.000000 -0.155408  0.009403  0.922721
  Pulse    -0.155408  1.000000  0.786535  0.025120
  Maxpulse  0.009403  0.786535  1.000000  0.203814
  Calories  0.922721  0.025120  0.203814  1.000000
** ((the number varies from -1 o 1))
  The corr() method ignores "not numeric" columns.
  >> there are three type of correlation
>  > Perfect Correlation 
>  > Good Correlation
>  > Bad Correlation
>  >
>  >Perfect Correlation:
We can see that "Duration" and "Duration" got the number 1.000000, which makes sense, each column always has a perfect relationship with itself.

Good Correlation:
"Duration" and "Calories" got a 0.922721 correlation, which is a very good correlation, and we can predict that the longer you work out, the more calories you burn, and the other way around: if you burned a lot of calories, you probably had a long work out.

Bad Correlation:
"Duration" and "Maxpulse" got a 0.009403 correlation, which is a very bad correlation, meaning that we can not predict the max pulse by just looking at the duration of the work out, and vice versa.


::>> Pandas Plotting ::>>

for plotting graph plot() ;
import pandas as pd 
import matplotlib.pyplot as plt 
df = pd.read_csv('data.csv')
df.plot()
plt.show()

# Scatter plot ":
A scatter plot needs x and y axis :
kind ='scatter'

code ::>>
>> import pandas as pd
>> import matplotlib.pyplot as plt
>> df = pd.read_csv('data.csv')
>> df.plot(kind = 'scatter' , x = 'duration'  y = 'calories' )
>> plt.show()



