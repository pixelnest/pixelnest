# CSharp

## Coding style

### Indents

The code is indented by two soft tabs (= spaces). DO NOT use hard tab.

### Brackets

Insert a bracket after a new line character :

```
void PlayJourney()
{

}
```

### Regions

Each class must follow this structure, in the correct order :

```
// Copyright © 2013 Pixelnest Studio
// This file is subject to the terms and conditions defined in
// file 'LICENSE.md', which is part of this source code package.
using System;

namespace Pixelnest
{
  public class Journey
  {
    #region Nested
    #endregion
    
    #region Static
    #endregion
    
    #region Constants
    #endregion
    
    #region Members
    #endregion
    
    #region Constructors
    #endregion
    
    #region Methods
    #endregion
    
    #region Handlers
    #endregion
    
    #region Properties
    #endregion 
  }
}
```

`Constants` is optional but recommended. `Nested`, `Static` and `Handlers` are optionals. The others are mandatory, even if they are empty. 

**You must follow the order.**

Minimal :

```
#region Members
#endregion

#region Constructors
#endregion

#region Methods
#endregion

#region Properties
#endregion
```

### Comments

You must use the "//" form everywhere in the code. You should comment your code before each new block.

```
// Do something.
var ps3 = new PS3();
ps3.Start();

// Do something crucial.
ps3.Play("Journey");
```

Use the "//" form to comment blocks of code.

You must use the "///" form to document classes, methods, properties, etc. :

```
namespace Pixelnest
{
  /// <summary>
  ///
  /// </summary>
  public class Journey
  {
    /// <summary>
    ///
    /// </summary>
    /// <param name="arg"></param>
    public void PlayWith(string arg)
    {

    } 
	}
}
```

## Conventions

### Classes

A class name must be written like :

```
class ExampleClass
```

### Interfaces

An interface name must be written like :

```
interface IExampleInterface
```

### Constants and read-only variables

A constant must be written like :

```
type EXAMPLE_CONSTANT
```

### (Static/Instance) Members/Fields

A field must be written like :

```
(static) type exampleField
```

A field SHOULD NOT be public. Use a property instead. This rule does not apply with a Unity MonoBehaviour.

### Methods

All the methods, whether they are public, private or protected, must be written like :

```
type DoExample()
```

A method name must be composed of an infinitive verb followed by an eventual description.

There is two exceptions.

The first one is for a method that returns a boolean. You can use a third-person verb instead, like :

```
bool HasExample()
bool IsExample()
bool CanExample()
```

The second one is for a handler. You should use a "On" prefix, followed by a description and a verb in its passive form, like :

```
void OnExampleEnded()
```

### Properties

A property name must be written like :

```
type ExampleProperty
```

A property should not begin by a verb.

### Events

Events are put with the properties in the regions.
An event name must be written like :

```
event type MessageReceived
```

An event should not begin by a verb, but should finish by a verb (in its passive form most of the time, except for a pending task, like a background worker or a mouse movement).

## C# syntax

### Types

The C# language provides some ways to write certains types, like string or boolean. You should use the all-lowercase/keyword type if possible.

```
/* Correct : */
string example;
bool example;

/* Incorrect :*/
String example;
Boolean example;
```

### Anonymous functions and callbacks

If you want to use an anonymous function, you should use this syntax :

```
(args) =>
{

}
```