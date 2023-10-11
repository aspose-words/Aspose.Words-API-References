---
title: StructuredDocumentTagCollection.RemoveAt
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagCollection metod. Tar bort en strukturerad dokumenttagg vid det angivna indexet.
type: docs
weight: 80
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Tar bort en strukturerad dokumenttagg vid det angivna indexet.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Ett index i samlingen. |

### Exempel

Visar hur man tar bort strukturerad dokumenttagg.

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
// Ta bort den strukturerade dokumenttaggen med Id.
structuredDocumentTags.Remove(1691867797);
// Ta bort den strukturerade dokumenttaggen vid position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Se även

* class [StructuredDocumentTagCollection](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* hopsättning [Aspose.Words](../../../)


