---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.VariableCollection, efficiently manage and customize document variables for enhanced document automation and flexibility.
type: docs
weight: 7410
url: /net/aspose.words/variablecollection/
---
## VariableCollection class

A collection of document variables.

To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/net/work-with-document-properties/) documentation article.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Gets or a sets a document variable by the case-insensitive name. `null` values are not allowed as a right hand side of the assignment and will be replaced by empty string. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | Adds a document variable to the collection. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Removes all elements from the collection. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | Determines whether the collection contains a document variable with the given name. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all variable in the collection. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | Returns the zero-based index of the specified document variable in the collection. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | Removes a document variable with the specified name from the collection. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | Removes a document variable at the specified index. |

## Remarks

Variable names and values are strings.

Variable names are case-insensitive.

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
