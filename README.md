
# _Epicodus Codealong - C# Lists & Dicts_

## Lists

#### _Why Lists_
If we want to create a collection where we can add or remove items, we need to use a list. For example, we might want to create a groceryList which could have any number of items in it. A list is a collection, usually of a single data type (like string or int). Unlike an array, a list can dynamically change in length.

#### _Creating Lists_
1. Declare a List. We use the keyword List to create a List object. Notice this is capitalized, unlike data types like string or int.

2. Declare the data type it will contain. It's best practice to declare the data type in angle brackets after List as we do with List<string> in the example above.

3. Give it a variable name. In the example above, we gave our List the name groceryList.

4. Create a new instance of List using its constructor. Finally, we create our List using its constructor with the new keyword: new List<string>. The example above states groceryList will be a new List containing strings.

5. Add data. The curly brackets {} at the end are required, even if we're not adding anything to our list yet. We can also add data to this list.

#### _Adding Content to Lists_
Once we've created a List, we can call the Add() method to add items to the List:
```sh
> List<string> groceryList = new List<string> {};

> groceryList.Add("spaghetti");

> groceryList
{ "spaghetti" }

> groceryList.Add("tomatoes");

> groceryList
{ "spaghetti", "tomatoes" }

> groceryList.Add("basil");

> groceryList
{ "spaghetti", "tomatoes", "basil" }

> groceryList.Add("meatballs");

> groceryList
{ "spaghetti", "tomatoes", "basil", "meatballs" }
```

#### _Removing Content from Lists_
If we check our pantry and realize we already have basil, we can remove it from our grocery list. To remove an item from a List, we'll use the built-in Remove() method:
```sh
> groceryList.Remove("basil")

> groceryList
{ "spaghetti", "CANDY!", "meatballs" }
```
When we call Remove() on an item in a List, C# will return true if the item is found and removed. If the argument is not present in a List, C# will return false.

## Dicts

#### _Why Dictionaries_
Dictionaries are a bit like phone books. Just as a phone book stores pairs of names and phone numbers, a dictionary holds key-value pairs. With a phone book, we look up a number (value) by its key (a person's name).

#### _Creating Dictionaries_
The basic format for creating a dictionary looks like this:
```sh
Dictionary<string, string> dictionaryName = new Dictionary<string, string>() {};
```

Here are all the steps to creating our dictionary:

1. Declare a Dictionary. We start with the keyword Dictionary to inform C# we're creating a Dictionary object. Dictionary should be capitalized, not lowercased like string or int.

2. Determine what the Dictionary will contain. We then declare the type of data the dictionary will contain in angle brackets: Dictionary<string, string>. Because Dictionarys contain key-value pairs, we declare two data types here. The first is the data type keys will be. The second is the data type for values.

3. Give it a variable name. We'll save our Dictionary in a variable so we can store it and access it later. In the example above, we gave our Dictionary the variable name myDictionary.

4. Create a new Dictionary instance with its constructor. Similar to Lists from the last lesson, we use its constructor with the new keyword: new Dictionary<string, string>().

5. Add data. The curly brackets {} at the end are required. They contain the information we'd like to put in our Dictionary. This information is formatted in key-value pairs that are also in curly brackets. If we're creating an empty dictionary, we leave these empty.

#### _Retrieving Content from a Dictionary_
Make a new Dictionary:
```sh
>  Dictionary<string, int> cupcakeOrder = new Dictionary<string, int>() { {"vanilla", 12}, {"chocolate", 24}, {"raspberry", 6}, {"caramel apple", 36} };
```
In this case, our value is an int instead of a string. Each number is stored with its associated flavor of cupcake. When we get to the bakery, we can easily check how many of each type we need:
```sh
> cupcakeOrder["vanilla"] // How many vanilla cupcakes do we want?
12

> cupcakeOrder["chocolate"] // How many chocolate?
24

> cupcakeOrder["raspberry"]
6

> cupcakeOrder["caramel apple"]
36
```
#### _Adding Content to a Dictionary
Make a new dict:
```sh
> Dictionary<string, string> myDictionary = new Dictionary<string, string>() { {"A", "apple"}, {"B", "bear"} };
```
Add a new entry:
```sh
> myDictionary["C"] = "cat";
```
