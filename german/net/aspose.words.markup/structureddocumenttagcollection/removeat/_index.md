---
title: StructuredDocumentTagCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre strukturierten Dokument-Tags mühelos mit der RemoveAt-Methode. Entfernen Sie Tags schnell nach Index für eine optimierte Dokumentbearbeitung.
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
| index | Int32 | Ein Index zur Sammlung. |

## Beispiele

Zeigt, wie strukturierte Dokument-Tags entfernt werden.

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
// Entfernen Sie das strukturierte Dokument-Tag anhand der ID.
structuredDocumentTags.Remove(1691867797);
// Entfernen Sie das strukturierte Dokument-Tag an Position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Siehe auch

* class [StructuredDocumentTagCollection](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
