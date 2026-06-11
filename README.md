## PYTHON PROGRAMMING MODULE 5B
## NAME: HARSHINI R
## REGISTER NUMBER: 212223220033
## Ex 01: Column-wise Sorting of a 2D Array
##  Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

##  Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

##  Program
```
import numpy as np
a=np.array(eval(input()))
print("Given array ")
b=np.sort(a, axis=0)
print(f" {a}")
print("")
print(b)
```
## Output

<img width="496" height="381" alt="604180127-1b9179c8-4f75-4d5c-9786-71cffb524e29" src="https://github.com/user-attachments/assets/630a952b-4dfb-4428-97e3-81c44917c9fd" />


## Result
Thus the program was successfully executed.

# #  Ex 02: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

##  Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

##  Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

##  Program
```
import numpy as np
l1=eval(input())
l2=eval(input())
x=np.array(l1)
y=np.array(l2)
print(np.where(x>y))
print(np.where(x == y))
```

## Output

<img width="846" height="179" alt="604180380-1cd90467-060d-465a-920d-4a8ff6507696" src="https://github.com/user-attachments/assets/1f6022e5-05f6-4291-8a4b-24c841fc44fd" />

## Result
Thus the program was successfully executed.

## Ex 03: Replace the Second Column in a 2D Array

##  Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

##  Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

##  Program
```
import numpy as np
x=eval(input())
y=eval(input())
arr1=np.array(x)
arr2=np.array(y)
print("Printing Original array")
print(arr1)
deleting=np.delete(arr1,1,axis=1)
print("Array after deleting column 2 on axis 1")
print(deleting)
inserting=np.insert(deleting,1,arr2,axis=1)
print("Array after inserting column 2 on axis 1")
print(inserting)
```

## Output

<img width="753" height="488" alt="604180652-ec59f15c-ac2a-4164-84b6-8f914f6409ab" src="https://github.com/user-attachments/assets/578251aa-8c70-4035-9017-5a51e7d71b3c" />

## Result
Thus the program was successfully executed

# Ex 04: Create and Display a DataFrame with Custom Index Labels

##  Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

##  Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

##  Program
```
import pandas as pd
import numpy as np
data={
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],  'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}
labels=['a','b','c','d','e','f','g','h','i','j']
df1=pd.DataFrame(data,index=labels)
print(df1)
```
## Output

<img width="844" height="295" alt="604180944-a75825a6-d2a5-4298-970b-37b79a1e70bf" src="https://github.com/user-attachments/assets/263d50b2-9d70-4400-be9d-4efb05c92fa1" />


## Result
Thus the program was successfully executed.

# Ex 05: Join Two DataFrames Along Rows

##  AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

##  ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

##  Program
```
import pandas as pd
x=eval(input())
y=eval(input())
a1=pd.DataFrame(x)
a2=pd.DataFrame(y)
print("Original DataFrames:")
print(a1)
print("-------------------------------------")
print(a2,'\n')
result=pd.concat([a1,a2],axis=1)
print("Join the said two dataframes along columns:")
print(result)
```

## Output

<img width="750" height="432" alt="604181195-b08abda7-ab65-4cdc-b935-0acbc7e6fb63" src="https://github.com/user-attachments/assets/752f6046-c399-410f-a8de-b42f34b6c4ae" />


## Result
Thus the program was successfully executed.
