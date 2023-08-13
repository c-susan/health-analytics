# health-analytics
Primer assignment for HHA 504/507

## Summary 
(1) Created a number and string vaiable and added a print statement to run the two variables. 
```
total_cholesterol_level = 150
var1 = 'Your total cholesterol level is: '
print(var1, total_cholesterol_level)
```


(2) Created a list of different cholesterol levels. Included an if, elif, else, and print statements for each variable on the list. Each print statement will print: "Your total cholesterol level is: " plus the variable {var} and an end statement. 
+ For cholesterol levels less than 200, the end statement is: "You are healthy."
+ For cholesterol levels 200 - 239, the end statement is: "You have high cholesterol." 
+ For cholesterol levels greater than 239, the end statement is "Please consult with your doctor." 
```
Cholesterol_list = [100, 150, 200, 220, 250, 300]
for var in Cholesterol_list:
    if var < 200:
        print(f"Your total cholesterol level is: {var}. You are healthy. \n")
    elif var >= 200 and var <= 239: 
        print(f"Your total cholesterol level is: {var}. You have high cholesterol. \n")
    else: 
        print(f"Your total cholesterol level is: {var}. Please consult with your doctor. \n")
```


(3) Created a dictionary called 'patients' with 3 nested dictionaries. Each nested dictionary is named with a patient name and has 4 key:value pairs called age, gender, chart, and medications. A list is included in each nested dictionary called medications. 
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
