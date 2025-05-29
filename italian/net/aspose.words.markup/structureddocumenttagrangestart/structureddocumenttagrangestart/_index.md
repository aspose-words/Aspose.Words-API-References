---
title: StructuredDocumentTagRangeStart
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words per .NET
description: Crea una nuova istanza di StructuredDocumentTagRangeStart senza sforzo. Migliora la gestione dei tuoi documenti con questo potente costruttore per tag strutturati.
type: docs
weight: 10
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart constructor

Inizializza una nuova istanza di**Inizio intervallo tag documento strutturato** classe.

```csharp
public StructuredDocumentTagRangeStart(DocumentBase doc, SdtType type)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |
| type | SdtType | Tipo di nodo SDT. |

## Osservazioni

È possibile creare i seguenti tipi di SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

## Esempi

Mostra come creare/rimuovere il tag di un documento strutturato e il suo contenuto.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // Rimuove il tag del documento strutturato con intervallo, ma mantiene il contenuto al suo interno.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    rangeStart = InsertStructuredDocumentTagRanges(doc);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // Rimuove il tag del documento strutturato con intervallo e il contenuto al suo interno.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public StructuredDocumentTagRangeStart InsertStructuredDocumentTagRanges(Document doc)
{
    StructuredDocumentTagRangeStart rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);

    return rangeStart;
}
```

### Guarda anche

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
