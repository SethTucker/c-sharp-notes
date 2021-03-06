# Dictionary / Hash / Hash Table:
Holds a collection of key-value pairs called pairs.

Values are accessed by keys and that's all! It is unordered.  
Dictionaries are imported with ```using System.Collections.Generic;```

<br>

#### Create a dictionary:
```c#
Dictionary<keytype, valuetype> dictName = new Dictionary<keytype, valuetype>();
```
```c#
// Declare with values
var dictName = new Dictionary<string, int>
{
    ["one"] = 1,
    ["two"] = 2,
    ["three"] = 3
};
```
```c#
// Create a dictionary from arrays or lists (using Linq's Enumerable)
using System.Linq;

// Arrays
var dictName = Enumerable.Range(0, keysArray.Length).ToDictionary(i => keysArray[i], i => valuesArray[i]);

// Lists
var dictName = Enumerable.Range(0, keysList.Count).ToDictionary(i => keysList[i], i => valuesList[i]);
```

<br>

#### Access a value using its key:
```c#
// value == dictName[key]

dictName[key];
```

<br>

#### Check if a key or value is in a dictionary:
```c#
Console.WriteLine(dictName.ContainsKey(key));

Console.WriteLine(dictName.ContainsValue(value));
```

<br>

#### Adding, changing, or deleting pairs:
```c#
// Add to a dictionary
dictName.Add(key,value);


// Change a pair (adds the pair if it doesn't exist)
dictName[key] = value;


// Delete a pair
dictName.Remove(key);
```

<br>

#### Loop through a dictionary:
All items will be processed in random order. (maybe)
```c#
foreach (KeyValuePair<keytype, valuetype> pair in dictName)
{
    Console.WriteLine($"Key: {pair.Key}, Value: {pair.Value}");
}


// Only keys
foreach (keytype key in dictName.Keys)
{
    Console.WriteLine($"Key: {key}");
}

// Only values
foreach (valuetype value in dictName.Values)
{
    Console.WriteLine($"Value: {value}");
}
```
