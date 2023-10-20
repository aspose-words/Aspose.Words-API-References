---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: StructuredDocumentTagCollection Remove methode. Entfernt das strukturierte DokumentTag mit der angegebenen Kennung in C#.
type: docs
weight: 70
url: /de/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Entfernt das strukturierte Dokument-Tag mit der angegebenen Kennung.

```csharp
public void Remove(int id)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | Int32 | Die Tag-ID des strukturierten Dokuments. |

## Beispiele

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
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
