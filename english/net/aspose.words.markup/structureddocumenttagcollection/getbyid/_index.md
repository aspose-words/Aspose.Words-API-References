---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words for .NET
description: Retrieve structured document tags effortlessly with the GetById method. Access your data quickly and enhance document management efficiency.
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
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Get the structured document tag or ranged tag by Title.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### See Also

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
