---
title: StructuredDocumentTagRangeStart.RemoveAllChildren
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTagRangeStart methode. Entfernt alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs.
type: docs
weight: 230
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/removeallchildren/
---
## StructuredDocumentTagRangeStart.RemoveAllChildren method

Entfernt alle Knoten zwischen diesem Startknoten des Bereichs und dem Endknoten des Bereichs.

```csharp
public void RemoveAllChildren()
```

### Beispiele

Zeigt, wie strukturierte Dokument-Tags und deren Inhalt erstellt/entfernt werden.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // Entfernt bereichsbezogenes strukturiertes Dokument-Tag, behält aber Inhalt darin.
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

    // Entfernt bereichsbezogenes strukturiertes Dokument-Tag und Inhalt darin.
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

* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* Montage [Aspose.Words](../../../)


