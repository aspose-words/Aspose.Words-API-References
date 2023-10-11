---
title: StructuredDocumentTagCollection.Remove
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagCollection metod. Tar bort den strukturerade dokumenttaggen med den angivna identifieraren.
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
| id | Int32 | Den strukturerade dokumenttaggens identifierare. |

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


