# functions
# Functions
def add(a,b):
    return a+b
student1=int(input("Enter the money:"))
student2=int(input("Enter the money:"))
total=add(student1,student2)
print("total amount:",total)
OUTPUT:
      Enter the money:3000
      Enter the money:4000
      total amount: 7000
---------------------------------------------------------------
  ef value():
    return 3.14159
result=value()
print("value in the function is",result)
 OUTPUT:   value in the function is 3.14159
 ------------------------------------------------------------
 def get_name():
    name=input("Enter your name:")
    return name
username=get_name()
print("WElCOME",username)
OUTPUT:
Enter your name: Y.S.JAGANMOHAN REDDY
WElCOME Y.S.JAGANMOHAN REDDY
-----------------------------------------------------------------
def info(name='unknown',age=0):
    print("Name:",name)
    print("Age:",age)
info("Gopi",21)
info("Chandu")
info(age=21)
info()
OUTPUT:
Name: Gopi
Age: 21
Name: Chandu
Age: 0
Name: unknown
Age: 21
Name: unknown
Age: 0
--------------------------------------------------------------------
def cal(a,b):
    return a+b,a-b,a*b,a/b
a=int(input("Enter a:"))
b=int(input("Enter b:"))
sum,diff,pro,div=cal(a,b)     
print("Sum",sum)
print("Subtract",diff)
print("Product",pro)
print("Divide",div)
OUTPUT:
Enter a: 44
Enter b: 2
Sum 46
Subtract 42
Product 88
Divide 22.0
--------------------------------------------------------------------------
 def eo(numbers):
    e=0
    o=0
    for n in numbers:
        if n %2==0:
            e+=1
        else:
            o+=1
    return e,o
num=input("Enter number of space seperated:")
num_list=list(map(int,num.split()))
e,o=eo(num_list)
print("Even Count:",e)
print("Odd Count:",o)
OUTPUT:
Enter number of space seperated: 8 66 90 888 45 2 167 46 
Even Count: 6
Odd Count: 2
----------------------------------------------------------------------------
def outer():
    print("This is a outer function.......")
    def inner():
        print("this is an inner function........")
    inner()
outer()   
OUTPUT:
This is a outer function.......
this is an inner function........
-----------------------------------------------------------------------------------
def cal(a,b):
    def add():
        return a+b
    def sub():
        return a-b
    def mul():
        return a*b
    print("Addition",add())
    print("Subtract",sub())
    print("product",mul())
a=int(input("Enter a number:"))
b=int(input("Enter a number:"))
cal(a,b)
OUTPUT:
Enter a number: 5
Enter a number: 5
Addition 10
Subtract 0
product 25
-------------------------------------------------------------------------------------------
def mul_by(n):
    def inner(x):
        return x*n
    return inner
times_2= mul_by(2)
times_3= mul_by(3)
print(times_2(5))
print(times_3(10))
 OUTPUT:
 10
30
-----------------------------------------------------------------------------------------
def greet(text):
    def inner(name):
        return f"{text},{name}!!!!!!"
    return inner 
hi=greet('Hello')
print(hi('Yaar'))
OUTPUT:
Hello,Yaar!!!!!!
-------------------------------------------------------------------------------------
fact=1
def factorial(n):
    global fact
    fact=1
    for i in range(1,n+1):
        fact*=i
    return fact
num=int(input("Enter a number:"))
if num<0:
    print("cannot derive for -ve number")
else:
    factorial (num)
    print(f"factorial of {num} is",fact )
OUTPUT:
Enter a number: 6
factorial of 6 is 720
------------------------------------------------------------------------------------
def factorial(n):
    if n==0 or n==1:
        return 1
    return n*factorial(n-1)
num=int(input("Enter the value:"))
value = factorial(num)
print(value)
OUTPUT:
Enter the value: 4
24
------------------------------------------------------------------------------------
def sum(n):
    if n==0:
        return 0
    return n+sum(n-1)
num=int(input("enter the number"))
print(f"sum of first {num} numbers is {sum(num)}")
OUTPUT:
enter the number 2
sum of first2 numbers is 3
------------------------------------------------------------------------------------
