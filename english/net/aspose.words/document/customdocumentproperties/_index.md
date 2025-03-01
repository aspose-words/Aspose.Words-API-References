---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words for .NET
description: Explore the CustomDocumentProperties property to access and manage all custom document properties efficiently, enhancing your document's functionality.
type: docs
weight: 80
url: /net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Returns a collection that represents all the custom document properties of the document.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
