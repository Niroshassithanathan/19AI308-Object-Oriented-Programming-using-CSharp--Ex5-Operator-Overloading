# 19AI308-Object-Oriented-Programming-using-CSharp--Ex5-Operator-Overloading

# AIM:
To write a C# program to pass values through constructors(default and parameterized) and also overload equal operators by checking whether objects 
are equal using operator overloading. 

# ALGORITHM:
### Step 1:
Initialize a default and a parameterized constructor.

### Step 2:
Overload using equalto symbols.

### Step 3:
Write the code to implement main function.

### Step 4:
Create objects obj1,obj2 and obj3.

### Step 5:
Check the equality.

# PROGRAM:
```
DEVELOPED BY : NIROSHA S
REGISTER NO : 212222230097
```
```c#
using System;

class MyClass
{
    private int value;

    public MyClass()
    {
        this.value = 0;
    }

    public MyClass(int value)
    {
        this.value = value;
    }

    
    public int GetValue()
    {
        return value;
    }
    public static bool operator ==(MyClass obj1, MyClass obj2)
    {

        
        if (obj1 is null || obj2 is null)
            return false;

        
        return obj1.value == obj2.value;
    }

  
    public static bool operator !=(MyClass obj1, MyClass obj2)
    {
        return !(obj1 == obj2);
    }
}

class Program
{
    static void Main(string[] args)
    {
        MyClass obj1 = new MyClass(10);
        MyClass obj2 = new MyClass(); 
        MyClass obj3 = new MyClass(10);

       
        Console.WriteLine("Are obj1 and obj2 equal? " + (obj1 == obj2));
        Console.WriteLine("Are obj1 and obj3 equal? " + (obj1 == obj3));
    }
}
```
# OUTPUT:
<img width="422" alt="image" src="https://github.com/Niroshassithanathan/19AI308-Object-Oriented-Programming-using-CSharp--Ex5-Operator-Overloading/assets/121418437/ee350361-6de0-40d6-9e8d-1931bfa09c13">


# RESULT:
Thus,the program to illustrate operating overloading is successfully implemented.
