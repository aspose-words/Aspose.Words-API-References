---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Ta enkelt bort specifika strukturerade dokumenttaggar med hjälp av metoden StructuredDocumentTagCollection Remove för effektiv dokumenthantering.
type: docs
weight: 70
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Tar bort den strukturerade dokumenttaggen med den angivna identifieraren.

```csharp
public void Remove(int id)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | Int32 | Taggidentifieraren för det strukturerade dokumentet. |

## Exempel

Visar hur man tar bort taggen för strukturerat dokument.

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
// Ta bort taggen för det strukturerade dokumentet med Id.
structuredDocumentTags.Remove(1691867797);
// Ta bort taggen för det strukturerade dokumentet vid position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Se även

* class [StructuredDocumentTagCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
