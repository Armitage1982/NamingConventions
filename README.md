# C# Naming Conventions

Based on Microsoft documentation [Capitalization Conventions](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/capitalization-conventions) & Hr Rony [Article on C# Corner](https://www.c-sharpcorner.com/article/stop-use-var-everywhere-and-think-before-use-underscore-with-private-variable-in/) 

___

| Object Name               | Notation   | Example                                                                              |
|:--------------------------|:-----------|--------------------------------------------------------------------------------------
| Namespace                 | PascalCase | ```namespace System.Security { ... }``` |
| Class                     | PascalCase | ```public class StreamReader { ... }``` |
| Constructor               | PascalCase | ```public class Person { public Person(string lastName, string firstName) { ... }}``` |
| Interface                 | PascalCase | ```public interface IEnumerable { ... }``` |
| Method                    | PascalCase | ```public class Object { public virtual string ToString(); }``` |
| Constants                 | PascalCase | ```public const int Months = 12;``` |
| struct                    | PascalCase | ```public struct Coords { ... }``` |
| Property                  | PascalCase | ```public string Name { get => name; }``` |
| Event                     | PascalCase | ```public class Process { public event EventHandler Exited; }``` |
| Delegate                  | PascalCase | ```public delegate void ProcessBookDelegate(Book book);``` |
| Enum value                | PascalCase | ```public enum FileMode { Alpha, Beta, Gamma }``` |
| Public Field              | PascalCase | ```public string Day;``` |
| **Private Field**         | **camelCase**  | ```private DateTime date;``` |
| **Parameter**             | **camelCase**  | ```public static class Convert { public static int ToInt32(string value); }``` |
| **Local variable**        | **camelCase**  | ```public class Object { public Do() { int index = 0; } }``` |

Basically use PascalCase everywhere except for parameters, local variable and Private Field.

**Private Field** is subject to many interpretations but I find this solution elegant and it works well with the Visual Studio encapsulation helper so I adopted it

___


## Why not using _underscore ?

![Alt text](/asset/underscore.png?raw=true "Why not using _underscore")

___


## How about Constructor then ?

![Alt text](/asset/constructor.png?raw=true "About Constructor")

___


## What about Var ?

I am also not inclined to use var outside LINQ and anonymous types

![Alt text](/asset/vargood.png?raw=true "Good use of var")

'var' should not be used in simple declarations, as shown below:

![Alt text](/asset/varbad.png?raw=true "Bad use of var")
