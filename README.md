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
