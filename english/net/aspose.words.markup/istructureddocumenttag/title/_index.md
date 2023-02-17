---
title: IStructuredDocumentTag.Title
second_title: Aspose.Words for .NET API Reference
description: IStructuredDocumentTag property. Specifies the friendly name associated with this SDT. Can not be null in C#.
type: docs
weight: 110
url: /net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Specifies the friendly name associated with this **SDT**. Can not be null.

```csharp
public string Title { get; set; }
```

## Examples

Shows how to get structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Get the structured document tag by Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Get the structured document tag or ranged tag by Title.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### See Also

* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../istructureddocumenttag/)
* assembly [Aspose.Words](../../../)
