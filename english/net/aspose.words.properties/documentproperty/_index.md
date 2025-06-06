---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Properties.DocumentProperty class for managing custom and built-in document properties efficiently. Enhance your document handling today!
type: docs
weight: 5200
url: /net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Represents a custom or built-in document property.

To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/net/work-with-document-properties/) documentation article.

```csharp
public class DocumentProperty
```

## Properties

| Name | Description |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Shows whether this property is linked to content or not. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Gets the source of a linked custom document property. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Returns the name of the property. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Gets the data type of the property. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Gets or sets the value of the property. |

## Methods

| Name | Description |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Returns the property value as bool. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Returns the property value as byte array. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Returns the property value as **DateTime** in UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Returns the property value as double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Returns the property value as integer. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Returns the property value as a string formatted according to the current locale. |

## Examples

Shows how to work with built-in document properties.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// The "Document" object contains some of its metadata in its members.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Some properties may store multiple values.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### See Also

* class [DocumentPropertyCollection](../documentpropertycollection/)
* namespace [Aspose.Words.Properties](../../aspose.words.properties/)
* assembly [Aspose.Words](../../)
