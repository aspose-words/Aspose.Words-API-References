---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words for .NET
description: Discover the GetByTitle method in StructuredDocumentTagCollection, which efficiently retrieves the first document tag by title for streamlined data management.
type: docs
weight: 50
url: /net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Returns the first structured document tag encountered in the collection with the specified title.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parameter | Type | Description |
| --- | --- | --- |
| title | String | The title of structured document tag. |

## Remarks

Returns null if the structured document tag with the specified title cannot be found.

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
