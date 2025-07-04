---
title: VariableCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words for .NET
description: Discover the VariableCollection IndexOfKey method. Quickly find the zero-based index of your document variable for efficient data management.
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

Assert.That(variables.Count, Is.EqualTo(3));

// We can display the values of variables in the document body using DOCVARIABLE fields.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.That(field.Result, Is.EqualTo("123 Main St."));

// Assigning values to existing keys will update them.
variables.Add("Home address", "456 Queen St.");

// We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
Assert.That(field.Result, Is.EqualTo("123 Main St."));

field.Update();

Assert.That(field.Result, Is.EqualTo("456 Queen St."));

// Verify that the document variables with a certain name or value exist.
Assert.That(variables.Contains("City"), Is.True);
Assert.That(variables.Any(v => v.Value == "London"), Is.True);

// The collection of variables automatically sorts variables alphabetically by name.
Assert.That(variables.IndexOfKey("Bedrooms"), Is.EqualTo(0));
Assert.That(variables.IndexOfKey("City"), Is.EqualTo(1));
Assert.That(variables.IndexOfKey("Home address"), Is.EqualTo(2));

Assert.That(variables[0], Is.EqualTo("3"));
Assert.That(variables["City"], Is.EqualTo("London"));

// Enumerate over the collection of variables.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Below are three ways of removing document variables from a collection.
// 1 -  By name:
variables.Remove("City");

Assert.That(variables.Contains("City"), Is.False);

// 2 -  By index:
variables.RemoveAt(1);

Assert.That(variables.Contains("Home address"), Is.False);

// 3 -  Clear the whole collection at once:
variables.Clear();

Assert.That(variables.Count, Is.EqualTo(0));
```

### See Also

* class [VariableCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
