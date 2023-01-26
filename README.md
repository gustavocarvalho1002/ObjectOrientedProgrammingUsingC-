# PILLARS OF OBJECT ORIENTED PROGRAMMING USING C#

## **Encapsulation**

Encapsulation is a way to restrict the direct access to some components of an object. In the example below, you can notice that the property  `Balance` is `private`. It means that it can only be accessed by code within the same class, as you can see in the methods `SetBalance` and `GetBalance`, but it won't let you access the property  `Balance` in the `Main()`.

```csharp
public class BankAccount
{
    private double Balance; //private atribute

    public double SetBalance(double balance) //public method
    {
        this.Balance = balance;
    }

    public double GetBalance() //public method
    {
        return Balance;
    }
}

public static void Main()
{
    BankAccount obj = new BankAccount();
    double currentBalance = obj.GetBalance();
}

```

## **Inheritance**

Inheritance is a feature of object-oriented programming languages that allows you to define a base class that provides specific functionality (data and behavior) and to define derived classes that either inherit or override that functionality (*[Microsoft,2022](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/inheritance)*).

```csharp
//base class Shape
class Shape
{
    public int Width;
    public int Height;
    public string Color;

    public void SetWidth(int w)
    {
        width = w;
    }
    public void SetHeight(int h)
    {
        height = h;
    }
}

//derived class Square  
class Square : Shape
{
    public int GetArea()
    {
        return width * height;
    }

}

public static void Main()
{
    Square square= new Square();
    square.SetHeight(10); //Square object acessing a method declared in Shape class
    square.SetWidth(10); //Square object acessing a method declared in Shape class
}
```

## **Polymorphism**

Poly means many and Morph means forms. Polymorphism is the process in which an object or function take different forms (*[C#Corner,2016](https://www.c-sharpcorner.com/UploadFile/e6a07d/pillars-of-oop/)*). In the example below we have the `Add` method that holds the same name but with three different implementations.

```csharp
//Implementation of polymorphism using method overloading  
class Base  
{  
      public int Add(int num1,int num2)  
      {  
              return(num1+num2);  
       }  
      public int Add(double num1,double num2)  
      {  
              return(num1+num2);  
      }
      public int Add(float num1, float num2, float num3)  
      {  
              return(num1+num2+num3);  
      }   
}
```

