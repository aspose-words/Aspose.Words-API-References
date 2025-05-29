---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Range StructuredDocumentTags, som tillhandahåller en omfattande samling strukturerade dokumenttaggar, vilket förbättrar dokumentets organisation och funktionalitet.
type: docs
weight: 50
url: /sv/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Returnerar en`StructuredDocumentTags` samling som representerar alla strukturerade dokumenttaggar i intervallet.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

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

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
