# C# Naming Conventions

Based on Microsoft documentation [Capitalization Conventions | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/capitalization-conventions) & Hr Rony [Article on C# Corner](https://www.c-sharpcorner.com/article/stop-use-var-everywhere-and-think-before-use-underscore-with-private-variable-in/) 

| Object Name               | Notation   | Example                                                                              |
|:--------------------------|:-----------|--------------------------------------------------------------------------------------
| Namespace                 | PascalCase | namespace System.Security { ... } |
| Class                     | PascalCase | public class StreamReader { ... } |
| Constructor               | PascalCase | public class Person { public Person(string lastName, string firstName) { ... } } |
| Interface                 | PascalCase | public interface IEnumerable { ... } |
| Method                    | PascalCase | public class Object { public virtual string ToString(); } |
| Constants                 | PascalCase | public const int months = 12; |
| struct                    | PascalCase | public struct Coords { ... } |
| Properties                | PascalCase | public string Name { get => name; } |
| Delegate                  | PascalCase | public delegate void ProcessBookDelegate(Book book); |
| Enum value                | PascalCase | public enum FileMode { Alpha, Beta, Gamma } |
| Public Field              | PascalCase | public string Day; |
| **Private Field**         | **camelCase**  | private DateTime date; |
| **Parameter**             | **camelCase**  | public static class Convert { public static int ToInt32(string value); } |
| **Local variable**        | **camelCase**  | public class Object { public Do() { int index = 0; } } |

Basically use PascalCase everywhere except for parameters, local variable and Private Field.
**Private Field** is subject to many interpretations but I find this solution elegant and it works well with Visual Studio encapsulation helper so I adopted it

## Why not using _underscore ?

![Alt text](/asset/underscore.png?raw=true "Why not using _underscore")

## How about Constructor then ?

![Alt text](/asset/constructor.png?raw=true "About Constructor")

## What about Var ?

I am also not inclined to use var outside LINQ and anonymous types
![Alt text](/asset/vargood.png?raw=true "Good use of var")

'var' should not be used in simple declarations, as shown below:
![Alt text](/asset/varbad.png?raw=true "Bad use of var")
