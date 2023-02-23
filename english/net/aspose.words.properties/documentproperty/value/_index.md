---
title: DocumentProperty.Value
linktitle: Value
second_title: Aspose.Words for .NET API Reference
description: DocumentProperty property. Gets or sets the value of the property in C#.
type: docs
weight: 50
url: /net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Gets or sets the value of the property.

```csharp
public object Value { get; set; }
```

## Remarks

Cannot be `null`.

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

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../documentproperty/)
* assembly [Aspose.Words](../../../)
