---
title: StructuredDocumentTagRangeStart.StructuredDocumentTagRangeStart
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagRangeStart constructor. Inicializa una nueva instancia del Comienzo del rango de etiquetas de documentos estructurados clase.
type: docs
weight: 10
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart constructor

Inicializa una nueva instancia del **Comienzo del rango de etiquetas de documentos estructurados** clase.

```csharp
public StructuredDocumentTagRangeStart(DocumentBase doc, SdtType type)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| type | SdtType | Tipo de nodo SDT. |

### Observaciones

Se pueden crear los siguientes tipos de SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* asamblea [Aspose.Words](../../../)


