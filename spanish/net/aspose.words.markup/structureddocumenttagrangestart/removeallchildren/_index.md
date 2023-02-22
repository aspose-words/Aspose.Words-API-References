---
title: StructuredDocumentTagRangeStart.RemoveAllChildren
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagRangeStart método. Elimina todos los nodos entre este nodo inicial de rango y el nodo final de rango.
type: docs
weight: 230
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/removeallchildren/
---
## StructuredDocumentTagRangeStart.RemoveAllChildren method

Elimina todos los nodos entre este nodo inicial de rango y el nodo final de rango.

```csharp
public void RemoveAllChildren()
```

### Ejemplos

Muestra cómo crear/eliminar una etiqueta de documento estructurado y su contenido.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // Elimina la etiqueta del documento estructurado por rangos, pero mantiene el contenido dentro.
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

    // Elimina la etiqueta del documento estructurado por rangos y el contenido interno.
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

### Ver también

* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* asamblea [Aspose.Words](../../../)


