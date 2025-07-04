---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access DocumentProperty objects effortlessly with our DocumentPropertyCollection Item. Retrieve properties by name for seamless document management.
type: docs
weight: 20
url: /net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Returns a [`DocumentProperty`](../../documentproperty/) object by the name of the property.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parameter | Description |
| --- | --- |
| name | The case-insensitive name of the property to retrieve. |

## Remarks

Returns `null` if a property with the specified name is not found.

## Examples

Shows how to create a custom document property which contains a date and time.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Returns a [`DocumentProperty`](../../documentproperty/) object by index.

```csharp
public DocumentProperty this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | Zero-based index of the [`DocumentProperty`](../../documentproperty/) to retrieve. |

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
* class [DocumentPropertyCollection](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
