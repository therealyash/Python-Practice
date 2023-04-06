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


