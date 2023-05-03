---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTagCollection GetById method. Returns the structured document tag by identifier in C#.
type: docs
weight: 30
url: /net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Returns the structured document tag by identifier.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | Int32 | The structured document tag identifier. |

## Remarks

Returns null if the structured document tag with the specified identifier cannot be found.

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

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* assembly [Aspose.Words](../../../)
