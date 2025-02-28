---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words for .NET
description: Discover the Range StructuredDocumentTags property, which provides a comprehensive collection of structured document tags, enhancing your document's organization and functionality.
type: docs
weight: 50
url: /net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Returns a `StructuredDocumentTags` collection that represents all structured document tags in the range.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## Examples

Shows how to remove structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Remove the structured document tag by Id.
structuredDocumentTags.Remove(1691867797);
// Remove the structured document tag at position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### See Also

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
