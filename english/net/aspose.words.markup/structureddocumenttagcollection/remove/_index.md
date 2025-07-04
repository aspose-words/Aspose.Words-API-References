---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove specific structured document tags using the StructuredDocumentTagCollection Remove method for streamlined document management.
type: docs
weight: 70
url: /net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Removes the structured document tag with the specified identifier.

```csharp
public void Remove(int id)
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | Int32 | The structured document tag identifier. |

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
Assert.That(sdt.Id, Is.EqualTo(1691867797));

Assert.That(structuredDocumentTags.Count, Is.EqualTo(5));
// Remove the structured document tag by Id.
structuredDocumentTags.Remove(1691867797);
// Remove the structured document tag at position 0.
structuredDocumentTags.RemoveAt(0);
Assert.That(structuredDocumentTags.Count, Is.EqualTo(3));
```

### See Also

* class [StructuredDocumentTagCollection](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
