# health-analytics
Primer assignment for HHA 504/507

## Summary 
(1) Imported pandas as pd and numpy as np as per the directions.
```
import pandas as pd 
import numpy as np 
```
<br>

(2) Created a number and string variable and added a print statement to run the two variables. 
```
total_cholesterol_level = 150
var1 = 'Your total cholesterol level is: '
print(var1, total_cholesterol_level, '\n','\n')
```
<br>

(3) Created a list of different cholesterol levels. Included an if, elif, else, and print statements for each variable on the list. Each print statement will print: "Your total cholesterol level is: " plus the variable {var} and an end statement. 
+ For cholesterol levels less than 200, the end statement is: "You are healthy."
+ For cholesterol levels 200 - 239, the end statement is: "You are at-risk for high cholesterol." 
+ For cholesterol levels greater than 239, the end statement is "You have high cholesterol." 
```
Cholesterol_list = [100, 150, 200, 220, 250, 300]
for var in Cholesterol_list:
    if var < 200:
        print(f"Your total cholesterol level is: {var}. You are healthy.")
    elif var >= 200 and var <= 239: 
        print(f"Your total cholesterol level is: {var}. You are at-risk for high cholesterol.")
    else: 
        print(f"Your total cholesterol level is: {var}. You have high cholesterol.")
print('\n \n')
```
<br>

(4) Created a dictionary called 'patients' with 3 nested dictionaries. Each nested dictionary is named with a patient name and has 4 key:value pairs called age, gender, chart, and medications. A list is included in each nested dictionary called medications. 
```
patients = {
    'Emma': {
        'age': 20,
        'gender': 'Female',
        'chart': {'Temperature': 96, 'Height': "5'4", 'Weight': '120lbs'},
        'medications': ['Ibuprofen', 'Omeprazole', 'Ferrous Sulfate'] 
    },
    'Daniel': {
        'age': 19,
        'gender': 'Male',
        'chart': {'Temperature': 96.5, 'Height': "6'1", 'Weight': '150lbs'},
        'medications': ['Tylenol', 'Omeprazole', 'Albuterol']
    },
    'Morgan': {
        'age': '30',
        'gender': 'Female',
        'chart': {'Temperature': 95, 'Height': "5'5", 'Weight': '120lbs'},
        'medications': ['Benzonante', 'Loratadine', 'Amoxicillin'] 
    }
}
```
<br>

(5) Created a function to measure cholesterol level with if, elif, and else statements. The function takes in the variables: LDLcholesterol, HDLcholesterol, and triglycerideLevel. Cholesterol level is calculated by the equation:  totalCholesterol = LDLcholesterol + HDLcholesterol + (0.2 * triglycerideLevel)
+ If cholesterol level less than 200, the healthy, the function returns 'Healthy'.
+ If cholesterol levelis 200 - 239, the function returns 'At-Risk'.
+ If cholesterol level is greater than 239, the function returns 'High Cholesterol'.

Example data and a variable called "output" is created to return the function "cholesterol". Print statements at the end will print the total cholesterol level and the corresponding status, either 'Healthy', 'At-Risk', or 'High Cholesterol'. 
```
def cholesterol(LDLcholesterol, HDLcholesterol, triglycerideLevel):
    totalCholesterol = LDLcholesterol + HDLcholesterol + (0.2 * triglycerideLevel)
    if totalCholesterol < 200:
       status = 'Healthy'
    elif totalCholesterol >= 200 and totalCholesterol <= 239:
        status = 'At-Risk'
    else:
        status = 'High Cholesterol'
    return status

LDLinput = 150
HDLinput = 50
triglycerideInput = 100

output = cholesterol(LDLinput, HDLinput, triglycerideInput)

print("Your total cholesterol level is:", LDLinput + HDLinput + (0.2 * triglycerideInput))
print(f'Your status is: {output}')
```
Given the example data in section (5), the function will return the following: 
<img width="307" alt="Screenshot 2023-08-13 at 11 17 53 PM" src="https://github.com/c-susan/health-analytics/assets/123512714/6af79f9e-8537-4c6c-a106-8b2d7a6367c9">
<br>
<br>

Reference:
Cleveland Clinic. (n.d.). _Cholesterol numbers and what they mean_. Retrieved August 13, 2023, from https://my.clevelandclinic.org/health/articles/11920-cholesterol-numbers-what-do-they-mean

