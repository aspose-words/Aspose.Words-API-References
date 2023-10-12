---
title: StructuredDocumentTagRangeStart.Id
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagRangeStart propiedad. Especifica una identificación numérica persistente única de solo lectura para esta etiqueta de documento estructurado.
type: docs
weight: 40
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Especifica una identificación numérica persistente única de solo lectura para esta etiqueta de documento estructurado.

```csharp
public int Id { get; }
```

### Observaciones

El atributo de identificación deberá seguir estas reglas:

* El documento conservará los identificadores de etiqueta de documento estructurados solo si se clona todo el documento [`Clone`](../../../aspose.words/document/clone/).
* Durante[`ImportNode`](../../../aspose.words/documentbase/importnode/) El ID se conservará si la importación no causa conflictos con otros ID de etiquetas de documentos estructurados en el documento de destino.
* Si varios nodos de etiquetas de documentos estructurados especifican el mismo valor de número decimal para el atributo Id, , entonces la primera etiqueta de documento estructurado del documento mantendrá este Id. original, y todos los nodos de etiquetas de documentos estructurados posteriores tendrán nuevos identificadores asignados cuando el documento está cargado.
* Durante la etiqueta de documento estructurado independienteINodeCloningListener)operación se generará una nueva ID única para el nodo de etiqueta de documento estructurado clonado.
* Si no se especifica Id en el documento fuente, entonces el nodo de etiqueta del documento estructurado tendrá un nuevo identificador único asignado cuando se cargue el documento.

### Ejemplos

Muestra cómo obtener las propiedades de etiquetas de documentos estructurados de varias secciones.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Ver también

* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* asamblea [Aspose.Words](../../../)


