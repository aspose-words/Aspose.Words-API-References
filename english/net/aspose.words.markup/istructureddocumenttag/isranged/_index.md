---
title: IsRanged
second_title: Aspose.Words for .NET API Reference
description: IStructuredDocumentTag method. Returns true if this instance is a ranged structured document tag in C#.
type: docs
weight: 140
url: /net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Returns true if this instance is a ranged structured document tag.

```csharp
public bool IsRanged()
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
