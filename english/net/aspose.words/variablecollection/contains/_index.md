---
title: VariableCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words for .NET API Reference
description: VariableCollection Contains method. Determines whether the collection contains a document variable with the given name in C#.
type: docs
weight: 50
url: /net/aspose.words/variablecollection/contains/
---
## VariableCollection.Contains method

Determines whether the collection contains a document variable with the given name.

```csharp
public bool Contains(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | Case-insensitive name of the document variable to locate. |

### Return Value

`true` if item is found in the collection; otherwise, `false`.

## Examples

Shows how to work with a document's variable collection.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Every document has a collection of key/value pair variables, which we can add items to.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// We can display the values of variables in the document body using DOCVARIABLE fields.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Assigning values to existing keys will update them.
variables.Add("Home address", "456 Queen St.");

// We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Verify that the document variables with a certain name or value exist.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// The collection of variables automatically sorts variables alphabetically by name.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Enumerate over the collection of variables.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Below are three ways of removing document variables from a collection.
// 1 -  By name:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 -  By index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 -  Clear the whole collection at once:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### See Also

* class [VariableCollection](../)
* namespace [Aspose.Words](../../variablecollection/)
* assembly [Aspose.Words](../../../)
