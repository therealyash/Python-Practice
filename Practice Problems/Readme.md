# Python Practice Problems

#### 1. User will input (3ages).Find the oldest one

```
age = []
for i in range(1,4):
    a = int(input('Enter the age of {i} person: '.format(i=i)))
    age.append(a)
print("Oldest one is",max(age))

Enter the age of 1 person: 45
Enter the age of 2 person: 55
Enter the age of 3 person: 65
Oldest one is 65
```

#### 2. Write a program that will convert celsius value to fahrenheit¶
```
c_temp = float(input('Enter the temperature in Celsius: '))
print(((9/5) * c_temp) + 32)

Enter the temperature in Celsius: 30
86.0
```

#### 3. User will input (2numbers).Write a program to swap the numbers
```
a = int(input('Enter 1st number: '))
b = int(input('Enter 2nd number: '))
a,b = b,a
print('Swapped Numbers are',a,b)

Enter 1st number: 55
Enter 2nd number: 20
Swapped Numbers are 20 55
```

#### 4. Write a program that will give you the sum of 3 digits
```
num = int(input('Enter a 3 digit number: '))
num_str = str(num)
num_lst = [int(i) for i in num_str]
print("Sum of 3 digits entered is:",sum(num_lst))
  
Enter a 3 digit number: 456
Sum of 3 digits entered is: 15
```

#### 5. Write a program that will reverse a four digit number. Also it checks whether the reverse is true.
```
num = int(input("Enter a 4 digit number: "))
# ex -  4567
thousands = num // 1000
hundreds = (num // 100) % 10
tens = (num // 10) % 10
ones = num % 10

reverse_num = int(str(ones) + str(tens) + str(hundreds) + str(thousands))
print('Reversed Number:',reverse_num)

if reverse_num == num:
    print('Reverse is True')
else:
    print('Reverse Not True')
    
Enter a 4 digit number: 8889
Reversed Number: 9888
Reverse Not True
```
#### using a loop
```
num = int(input("Enter a four-digit number: "))

reverse_num = 0
temp = num

while temp > 0:
    digit = temp % 10
    reverse_num = (reverse_num * 10) + digit
    temp = temp // 10
    
    if temp == 0:
        print('Hi')

print("Reverse number is:", reverse_num)

if num == reverse_num:
    print("The reverse is true.")
else:
    print("The reverse is false.")
    
"""
Dry run

temp digit reverse_num

4567	7	7
456 	6 	76
45 		5 	765
4 		4 	7654
0.4

"""
Enter a four-digit number: 4567
Hi
Reverse number is: 7654
The reverse is false.
```

#### 6. Write a program that will tell whether the number entered by user is odd or even
```
num = int(input('Enter a number: '))
res = 'Even' if num % 2 == 0 else 'Odd'
print(res)
Enter a number: 25

Odd
```

#### 7. Write a program to check whether the given year is a leap year or not.
```
year = int(input('Enter an year: '))
# year evenly divisible by 4
# year not evenly divisible by 4
if year % 4 == 0:
    if year % 100 != 0:
        print('Leap Year!')
    else:
        print('Not a Leap Year!')
else:
    print('Not a Leap Year!')
    
Enter an year: 2024
Leap Year!
```

#### 8. Write a program to calculate Euclidean distance between 2 coordinates.
```
import math
print('Calculate Euclidean Distance between 2 Coordinates.')
x1 = int(input('Enter x1: '))
x2 = int(input('Enter x2: '))
y1 = int(input('Enter y1: '))
y2 = int(input('Enter y2: '))

d = round(math.sqrt (((x2-x1)**2) + ((y2-y1)**2)),2)
print('Euclidean Distance:', d)

Calculate Euclidean Distance between 2 Coordinates.
Enter x1: 2
Enter x2: 5
Enter y1: 4
Enter y2: 7
Euclidean Distance: 4.24
```

#### 9. Write a program that takes a user input of 3 angles and will find out whether it can form a triangle or not.
```
print('Triangle Check Program')
sum_ang = 0
for i in range(1,4):
    ang = round(float(input("Enter angle {}: ".format(i))))
    sum_ang = sum_ang + ang
if sum_ang == 180:
    print('Triangle Can be Formed!')
else:
    print('Triangle Cannot be Formed!')

Triangle Check Program
Enter angle 1: 60
Enter angle 2: 60
Enter angle 3: 60
Triangle Can be Formed!
```

#### 10. Write a program that take user input of cost price and selling price and determine whether it's a loss or a profit.
```
print('Profit or Loss!')
cost = float(input('Enter Cost Price: '))
sell = float(input('Enter Selling Price: '))
if (sell-cost) > 0:
    print('Profit!')
elif (sell - cost) == 0:
    print('No Profit No Loss!')
else:
    print('Loss!')
    
Profit or Loss!
Enter Cost Price: 500
Enter Selling Price: 900
```

#### 11. Write a program to find the simple interest when the value of principle rate of interest and time period is given.
```
print('Simple Interest Program!')
p = float(input('Please enter the principal amount: '))
r = round(float(input('Please enter annual interest rate: ')),2) * 0.01
t = int(input('Please enter years: '))

a = p*(1+(r*t))
print('Total amount after {} years is {}'.format(t,a))
print('Interest amount is {}'.format((a-p))

Simple Interest Program!
Please enter the principal amount: 1000
Please enter annual interest rate: 12
Please enter years: 5
Total amount after 5 years is 1600.0
Interest amount is 600.0
```




