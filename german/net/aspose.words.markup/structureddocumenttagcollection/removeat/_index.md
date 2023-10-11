---
title: StructuredDocumentTagCollection.RemoveAt
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagCollection methode. Entfernt ein strukturiertes DokumentTag am angegebenen Index.
type: docs
weight: 80
url: /de/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Entfernt ein strukturiertes Dokument-Tag am angegebenen Index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in die Sammlung. |

### Beispiele

Zeigt, wie man strukturierte Dokument-Tags entfernt.

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
// Entfernen Sie das strukturierte Dokument-Tag nach Id.
structuredDocumentTags.Remove(1691867797);
// Entfernen Sie das strukturierte Dokument-Tag an Position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Siehe auch

* class [StructuredDocumentTagCollection](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* Montage [Aspose.Words](../../../)


