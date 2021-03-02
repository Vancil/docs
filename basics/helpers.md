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

