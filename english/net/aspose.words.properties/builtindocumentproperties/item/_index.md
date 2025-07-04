---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access DocumentProperty objects effortlessly with the BuiltInDocumentProperties Item property. Streamline your document management today!
type: docs
weight: 140
url: /net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Returns a [`DocumentProperty`](../../documentproperty/) object by the name of the property.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parameter | Description |
| --- | --- |
| name | The case-insensitive name of the property to retrieve. |

## Remarks

The string names of the properties correspond to the names of the typed properties available from [`BuiltInDocumentProperties`](../).

If you request a property that is not present in the document, but the name of the property is recognized as a valid built-in name, a new [`DocumentProperty`](../../documentproperty/) is created, added to the collection and returned. The newly created property is assigned a default value (empty string, zero, `false` or DateTime.MinValue depending on the type of the built-in property).

If you request a property that is not present in the document and the name is not recognized as a built-in name, a `null` is returned.

## Examples

Shows how to work with custom document properties.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties. 
Assert.That(doc.CustomDocumentProperties["CustomProperty"].ToString(), Is.EqualTo("Value of custom document property"));

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
