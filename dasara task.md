26)YouTube Upload Count
You are given a list of dates in the format Dec 11 and a month in the format Dec as arguments. Each date represents a video that was uploaded on that day. Return the number of uploads for a given month.


```python
dates = ["may 22", "may 21", "dec 15"]
t_month = "may"
x = 0
for i in dates:
    z = dates[x].split()
    if len(z) == 2:
        month = z[0]
    if month == t_month:
            x+=1

print(x)
```

    2
    

27) Create a function that returns the sum of all even elements in a 2D matrix.


```python
rows = int(input("Enter the number of rows: "))   
cols = int(input("Enter the number of columns: "))

matrix = []        
row = 0

while row < rows:       
    col = 0
    matrix_row = []
    while col < cols:
        element = int(input(f"Enter the element at row {row + 1}, column {col + 1}: "))
        matrix_row.append(element)
        col += 1
    matrix.append(matrix_row)
    row += 1
         
print(f"The sum of even elements in the matrix is: {even_sum}")
```

    Enter the number of rows: 3
    Enter the number of columns: 3
    Enter the element at row 1, column 1: 1
    Enter the element at row 1, column 2: 2
    Enter the element at row 1, column 3: 3
    Enter the element at row 2, column 1: 4
    Enter the element at row 2, column 2: 5
    Enter the element at row 2, column 3: 5
    Enter the element at row 3, column 1: 1
    Enter the element at row 3, column 2: 6
    Enter the element at row 3, column 3: 5
    The sum of even elements in the matrix is: 20
    

28) Create a function that determines whether or not a list is a factor chain.


```python
numbers = input("Enter a list of numbers separated by spaces: ").split()

numbers = [int(num) for num in numbers]  

is_factor_chain = True


for i in range(1, len(numbers)):  
    if numbers[i] % numbers[i - 1] != 0:
        is_factor_chain = False
        break


if is_factor_chain: 
    print("True")
else:
    print("False")
```

    Enter a list of numbers separated by spaces: 1 5 99 100
    False
    

29) Create a function, that will for a given a, b, c, do the following:

Add a to itself b times.
Check if the result is divisible by c.


```python
a = int(input("Enter a value for 'a': "))
b = int(input("Enter a value for 'b': "))
c = int(input("Enter a value for 'c': "))

for i in range(b):                         
    a += a

is_divisible = a % c == 0                     
                                            
print(f"Is {a} + ({a} * {b}) divisible by {c} {  is_divisible  }") 
```

    Enter a value for 'a': 5
    Enter a value for 'b': 6
    Enter a value for 'c': 8
    Is 320 + (320 * 6) divisible by 8 True
    

30) Write a function that takes three arguments (x, y, z) and returns a list containing x sublists (e.g. [[], [], []]), each containing y number of item z.

x Number of sublists contained within the main list.
y Number of items contained within each sublist.
z Item contained within each sublist.


```python
x = int(input("Enter the number of sublists: "))
y = int(input("Enter the number of items in each sublist: "))
z = int(input("Enter the item value: "))

matrix = [] 

for _ in range(x): 
    
    row_data = [z] * y
    
    
    matrix.append(row_data)


print(matrix)
```

    Enter the number of sublists: 6
    Enter the number of items in each sublist: 4
    Enter the item value: 1
    [[1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1]]
    

31) The insurance guy calls again and apologizes. They found another policy made by your spouse, but this one is limited to cover a particular maximum in losses (for example, 50,000€). You send a bill to your spouse for the difference you lost.

Given a dict of the stolen items and a limit, return the difference between the total value of those items and the limit of the policy.


```python
obj = {}

for i in range(0,20):             
    key = input("Enter a key (or 'done' to finish): ")

    if key == 'done':
        break                                

    value = int(input(f"Enter the value for {key}: "))
    obj[key] = value

limit = int(input("Enter the limit: "))

total = sum(obj.values())
difference = total - limit

print(f"The difference between the sum of values and the limit is: {difference}")
```

    Enter a key (or 'done' to finish): python
    Enter the value for python: 10
    Enter a key (or 'done' to finish): 6
    Enter the value for 6: 2
    Enter a key (or 'done' to finish): 3
    Enter the value for 3: 1
    Enter a key (or 'done' to finish): done
    Enter the limit: 5
    The difference between the sum of values and the limit is: 8
    

32) There’s a great war between the even and odd numbers. Many numbers already lost their lives in this war and it’s your task to end this. You have to determine which group sums larger: the evens or the odds. The larger group wins.

Create a function that takes a list of integers, sums the even and odd numbers separately, then returns the difference between the sums of the even and odd numbers.


```python
input_numbers = input("Enter a list of numbers separated by spaces: ")
lst = [int(num) for num in input_numbers.split()]

even_sum = 0
odd_sum = 0

for num in lst:                     
    if num % 2 == 0:
        even_sum += num         
    else:
        odd_sum += num          
                                
result = abs(even_sum - odd_sum)  

print(result)
```

    Enter a list of numbers separated by spaces: 5 6 7 8
    2
    

33) Create a function that compares two words based on the sum of their ASCII codes and returns the word with the smaller ASCII sum.


```python
x = ["hello", "world"]
y = float('inf')  
z = None
i = 0
for word in x:
    word = x[i]
    word_sum = sum(ord(char) for char in word)
    if word_sum < y:
        y = word_sum
        z = word
    i += 1 
print(z)
```

    hello
    

34) Write a function that returns the longest sequence of consecutive zeroes in a binary string


```python
binary_string = "110100010000111000"

max_count = 0
current_count = 0

for digit in binary_string:
    if digit == '0':
        current_count += 1
        max_count = max(max_count, current_count)
    else:
        current_count = 0

print(max_count)
```

    4
    

35) Write a function that takes a string of one or more words as an argument and returns the same string, but with all five or more letter words reversed. Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.


```python
sentence = "This is a sample sentence with various words"

words = sentence.split()

for i in range(len(words)):
    if len(words[i]) >= 5:
        words[i] = words[i][::-1]

modified_sentence = ' '.join(words)
print(modified_sentence)
```

    This is a elpmas ecnetnes with suoirav sdrow
    

36) Create a function that returns the frequency distribution of a list. This function should return an object, where the keys are the unique elements and the values are the frequency in which those elements occur.


```python
lst = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]

freq_dict = {}

for item in lst:
    if item in freq_dict:
        freq_dict[item] += 1
    else:
        freq_dict[item] = 1

print(freq_dict)
```

    {1: 1, 2: 2, 3: 3, 4: 4}
    

37) Imagine a school that kids attend for 6 years. In each year, there are five groups started, marked with the letters a, b, c, d, e. For the first year, the groups are 1a, 1b, 1c, 1d, 1e and for the last year, the groups are 6a, 6b, 6c, 6d, 6e.


```python
all_groups = []

for year in range(1, 7):
    year_groups = [f"{year}{group}" for group in ['a', 'b', 'c', 'd', 'e']]
    all_groups.append(year_groups)

for year, groups in enumerate(all_groups, start=1):
    print(f"Year {year}: {', '.join(groups)}")
```

    Year 1: 1a, 1b, 1c, 1d, 1e
    Year 2: 2a, 2b, 2c, 2d, 2e
    Year 3: 3a, 3b, 3c, 3d, 3e
    Year 4: 4a, 4b, 4c, 4d, 4e
    Year 5: 5a, 5b, 5c, 5d, 5e
    Year 6: 6a, 6b, 6c, 6d, 6e
    

38) Create a function that takes a list of numbers and returns a list where each number is the sum of itself + all previous numbers in the list.


```python
numbers = [1, 2, 3, 4, 5]

list = []
sum = 0

for num in numbers:
    sum += num
    list.append(sum)

print(list)
```

    [1, 3, 6, 10, 15]
    

39) Create a function that accepts a string as an argument and returns the first non-repeated character.


```python
input_str = "examplestring"

char_count = {}

# Count occurrences of each character
for char in input_str:
    if char in char_count:
        char_count[char] += 1
    else:
        char_count[char] = 1

# Find the first character with count 1
for char in input_str:
    if char_count[char] == 1:
        print(f"The first non-repeated character is: {char}")
        break
else:
    print("No non-repeated character found")
```

    The first non-repeated character is: x
    

40) Create a function that returns True if an asterisk * is inside a box.


```python
box = "**** * ** ***"

if '*' in box:
    print("True - Asterisk is inside the box")
else:
    print("False - Asterisk is not inside the box")
```

    True - Asterisk is inside the box
    


```python

```
