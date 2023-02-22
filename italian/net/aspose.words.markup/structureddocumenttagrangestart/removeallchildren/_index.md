---
title: StructuredDocumentTagRangeStart.RemoveAllChildren
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagRangeStart metodo. Rimuove tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dellintervallo.
type: docs
weight: 230
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/removeallchildren/
---
## StructuredDocumentTagRangeStart.RemoveAllChildren method

Rimuove tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dell'intervallo.

```csharp
public void RemoveAllChildren()
```

### Esempi

Mostra come creare/rimuovere tag di documenti strutturati e il relativo contenuto.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // Rimuove il tag del documento strutturato a intervalli, ma mantiene il contenuto all'interno.
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

    // Rimuove il tag del documento strutturato a intervalli e il contenuto all'interno.
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

### Guarda anche

* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assemblea [Aspose.Words](../../../)


