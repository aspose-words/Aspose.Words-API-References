---
title: StructuredDocumentTagRangeStart.Tag
linktitle: Tag
articleTitle: Tag
second_title: Aspose.Words para .NET
description: Descubra la propiedad StructuredDocumentTagRangeStart para un etiquetado de documentos mejorado. Asocie etiquetas fácilmente con nodos para optimizar su flujo de trabajo.
type: docs
weight: 150
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/tag/
---
## StructuredDocumentTagRangeStart.Tag property

Especifica una etiqueta asociada con el nodo de etiqueta del documento estructurado actual. No se puede`nulo` .

```csharp
public string Tag { get; set; }
```

## Observaciones

Una etiqueta es una cadena arbitraria que las aplicaciones pueden asociar con una etiqueta de documento estructurado para identificarla sin proporcionar un nombre descriptivo visible.

## Ejemplos

Muestra cómo obtener las propiedades de las etiquetas de documentos estructurados de varias secciones.

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
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
