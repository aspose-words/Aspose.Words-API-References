---
title: VariableCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words for .NET
description: VariableCollection IndexOfKey method. Returns the zerobased index of the specified document variable in the collection in C#.
type: docs
weight: 70
url: /net/aspose.words/variablecollection/indexofkey/
---
## VariableCollection.IndexOfKey method

Returns the zero-based index of the specified document variable in the collection.

```csharp
public int IndexOfKey(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The case-insensitive name of the variable. |

### Return Value

The zero based index. Negative value if not found.

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

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

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

Assert.AreEqual(0, variables.Count);
```

### See Also

* class [VariableCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
