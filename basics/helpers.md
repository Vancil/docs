# Helpers

* [Introduction](helpers.md#introduction)
* [Available Functions](helpers.md#available-functions)

## Introduction

Vancil includes many global helper functions to use throughout your application.

## Available Functions

#### Strings

|  |  |  |
| :--- | :--- | :--- |
| [ClassBaseName](helpers.md#classbasename) |  |  |
| [After](helpers.md#after) |  |  |
| [AfterLast](helpers.md#afterlast) |  |  |
| [Before](helpers.md#before) |  |  |
| [BeforeLast](helpers.md#beforelast) |  |  |

#### \# ClassBaseName

Returns the class name of the given class with the class' namespace removed.

```csharp
new StringHelper().ClassBaseName("Foo.Bar.Baz")

// Baz
```

#### \# After

Returns everything after the given value of the string.

```csharp
new StringHelper().After("Hi, how are you", "Hi, how")

//" are you"
```

#### \# AfterLast

Returns everything after the last occurrence of the given string value.

```csharp
new StringHelper().AfterLast("Vancil.Project.Namespace", ".")

//"Namespace"
```

#### \# Before

Returns everything before the given value of the string.

```csharp
new StringHelper().Before("Hi, how are you", "are you")

//"Hi, how "
```

#### \# BeforeLast

Returns everything before the last occurrence of the given value in a string.

```csharp
new StringHelper().BeforeLast("Vancil.Project.Namespace", ".")

//"Vancil.Project"
```

