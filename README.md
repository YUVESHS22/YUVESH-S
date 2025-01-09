#lp1 
from math import pi
r=int(input("enter the radius of the circle:"))
a=pi*r**2
print(f"the area of the circle is {a}")


#lp2
n=input("Enter an integer number:")
nn=n*2
nnn=n*3
sum=int(n)+int(nn)+int(nnn)
print(f"the sum of {n}+{nn}+{nnn} is :{sum}")


#lp3
a=int(input("Enter the first number:"))
b=int(input("Enter the second number:"))
product=a*b
if product<=1000:
    result=product
else:
    result=a+b
print(f"The result is {result}")


#lp4
m=int(input("Enter the number to print multiplication table:"))
for count in range (1,11):
    print(m,"x",count,"=",m*count)


#lp5
number=(1,7,5,67,69,96,24,36)
countOdd=0
countEven=0
for x in number:
    if not x%2:
        countEven+=1
    else:
        countOdd+=1
print(f"The count of even numbers ={countEven}")
print(f"The count of odd numbers={countOdd}")


#lp6
celcius=float(input("Enter the temperature in celcius:"))
fahrenheit=(celcius*9/5)+32
print(f"The temperature in fahrenheit is {fahrenheit}")

fahrenheit=float(input("Enter the temperature in fahrneheit:"))
celcius=(fahrenheit-32)*5/9
print(f"The temperature in cecius is {celcius}")


#lp7
items=[n for n in input().split("-")]
items.sort()
print("-".join(items))


#lp8
inputString=input("Enter a string:")
countUpper=0
countLower=0
countSpaces=0
for i in inputString:
    if i.isupper():
        countUpper+=1
    elif i.islower():
        countLower+=1
    elif i.isspace():
        countSpaces+=1
print(f"Count of uppercase characters:{countUpper}")
print(f"Count of lowercase characters:{countLower}")
print(f"Count of spaces :{countSpaces}")
inputString=inputString.swapcase()
print(f"The toggled string is {inputString}")


#lp9
string=input("Enter a string:")
countDigits=0
countLetters=0
for i in string:
    if i.isalpha():
        countLetters+=1
    elif i.isdigit():
        countDigits+=1
print(f"The number of letters is {countLetters}")
print(f"The number of digits is {countDigits}")


#lp10
dict={0:10,
      1:20}
print(f"The dictionary before updation is {dict}")
dict.update({2:30})
print(f"The dictionary after updation is {dict}")


#lp11
set={1,2,3,4,5,6}
print(f"the set before deletion is {set}")
set.discard(4)
print(f"The set after discarding 4 is {set}")


#lp12
tup=(1,2,3,4,4,3,2,5,5,7,8,8,9)
count=tup.count(4)
print(f"The count of 4 is {count}")
count=tup.count(5)
print(f"The count of 5 is {count}")


#lp13
with open ("myfile.txt","r") as fp:
    lines=len(fp.readlines())
print("The total number of lines=",lines)
fp.close


#lp14
file1=open("file1","w")
l=["this i s delhi \n","this is paris\n","this is london \n"]
file1.writelines(l)
file1.close()
file1=open("file1","r")
print("output ofreadlines before appending:")
print(file1.read())
print()
file1=open("file1","a")
file1.write("today \n")
file1.close()
file1=open("file1","r")
print("outut of readlines after appending:")
print(file1.read())
print()
file1.close()


#lp15
import string,os
if not os.path.exists("letters"):
    os.makedirs("letters")
for letter in string.ascii_uppercase:
    with open("letters\\"+letter+".txt","w") as f:
        f.writelines(letter)