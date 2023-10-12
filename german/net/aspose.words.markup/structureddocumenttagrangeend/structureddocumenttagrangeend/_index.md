---
title: StructuredDocumentTagRangeEnd.StructuredDocumentTagRangeEnd
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagRangeEnd constructeur. Initialisiert eine neue Instanz von Ende des TagBereichs des strukturierten Dokuments Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.markup/structureddocumenttagrangeend/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd constructor

Initialisiert eine neue Instanz von **Ende des Tag-Bereichs des strukturierten Dokuments** Klasse.

```csharp
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| id | Int32 | Bezeichner des entsprechenden Tagbereichsanfangs des strukturierten Dokuments. |

### Beispiele

Zeigt, wie strukturierte Dokument-Tags und deren Inhalt erstellt/entfernt werden.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // Entfernt das strukturierte Dokument-Tag, behält aber den Inhalt bei.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    InsertStructuredDocumentTagRanges(doc, out rangeStart);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // Entfernt strukturierte Dokument-Tags und Inhalte darin.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public void InsertStructuredDocumentTagRanges(Document doc, out StructuredDocumentTagRangeStart rangeStart)
{
    rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);
}
```

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [StructuredDocumentTagRangeEnd](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* Montage [Aspose.Words](../../../)


