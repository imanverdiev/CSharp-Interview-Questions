# CSharp Interview Questions by Emin Imanverdiyev

## 1. How is C# different from C?
C is a procedural language, while C# is an object-oriented language. The biggest difference is that C# supports automatic garbage collection through the Common Language Runtime (CLR), whereas C does not. C# primarily requires the .NET framework to execute, while C is a platform-agnostic language.

## 2. What is inheritance? Does C# support multiple inheritance?
Inheritance means acquiring some of the properties from a master class. 

![image](https://github.com/user-attachments/assets/33204787-d62c-4ef2-967f-13ff7914c2a3)

Also, C# doesn’t support multiple inheritances. 
Instead, you can use interfaces to inherit the properties using the class name in the signature.

Here, class C can inherit properties from Class A and Class B.

### Example of Inheritance:

```csharp
// C# program to illustrate multiple class inheritance
using System;
using System.Collections;

// Parent class 1
class Scaler
{
    // Providing the implementation of features() method
    public void features()
    {
        // Creating ArrayList
        ArrayList My_features = new ArrayList();

        // Adding elements in the My_features ArrayList
        My_features.Add("Abstraction");
        My_features.Add("Encapsulation");
        My_features.Add("Inheritance");

        Console.WriteLine("Features provided by OOPS:");
        foreach (var elements in My_features)
        {
            Console.WriteLine(elements);
        }
    }
}

// Parent class 2
class Scaler2 : Scaler
{
    // Providing the implementation of languages() method
    public void languages()
    {
        // Creating ArrayList
        ArrayList My_features = new ArrayList();

        // Adding elements in the My_features ArrayList
        My_features.Add("C++");
        My_features.Add("C#");
        My_features.Add("JScript");

        Console.WriteLine("\nLanguages that use OOPS concepts:");
        foreach (var elements in My_features)
        {
            Console.WriteLine(elements);
        }
    }
}

// Child class
class ScalertoScaler : Scaler2
{
}

// Main method
public class Scaler1
{
    static public void Main()
    {
        // Creating object of ScalertoScaler class
        ScalertoScaler obj = new ScalertoScaler();
        obj.features();
        obj.languages();
    }
}
````
## 3. What is the difference between an Array and ArrayList in C#?
An array is a collection of similar variables clubbed together under one common name. While ArrayList is a collection of objects that can be indexed individually. With ArrayList, you can access a number of features like dynamic memory allocation, adding, searching, and sorting items in the ArrayList.

- When declaring an array, the size of the items is fixed, therefore, the memory allocation is fixed. But with ArrayList, it can be increased or decreased dynamically.
- Array belongs to the `System.Array` namespace while ArrayList belongs to the `System.Collections` namespace.
- All items in an array are of the same datatype while all the items in an ArrayList can be of the same or different data types.
- Arrays cannot accept null, while ArrayList can accept null values.

### Example:

```csharp
// C# program to illustrate the ArrayList
using System;
using System.Collections;
 
class IB {
 
   // Main Method
   public static void Main(string[] args)
   {
       // Create a list of strings
       ArrayList al = new ArrayList();
       al.Add("Bruno");
       al.Add("Husky");
       al.Add(10);
       al.Add(10.10);
 
       // Iterate list element using foreach loop
       foreach(var names in al)
       {
           Console.WriteLine(names);
       }
````
## 4. What are Generics in C#?
In C# collections, defining any kind of object is termed okay which compromises C#’s basic rule of type-safety. Therefore, generics were included to type-safe the code by allowing re-use of the data processing algorithms. Generics in C# mean not linked to any specific data type. Generics reduce the load of using boxing, unboxing, and typecasting objects. Generics are always defined inside angular brackets `<>`.

To create a generic class, this syntax is used:

```csharp
GenericList<float> list1 = new GenericList<float>();
GenericList<Features> list2 = new GenericList<Features>();
GenericList<Struct> list3 = new GenericList<Struct>();
````
Here, GenericList<float> is a generic class. In each of these instances of GenericList<T>, every occurrence of T in the class is substituted at run time with the type argument. By substituting the T, we have created three different type-safe uses of the same class.


   }
}
