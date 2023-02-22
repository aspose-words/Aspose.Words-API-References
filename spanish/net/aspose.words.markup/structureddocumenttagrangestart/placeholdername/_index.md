---
title: StructuredDocumentTagRangeStart.PlaceholderName
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagRangeStart propiedad. Obtiene o establece el Nombre delBuildingBlock que contiene texto de marcador de posición.
type: docs
weight: 120
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/placeholdername/
---
## StructuredDocumentTagRangeStart.PlaceholderName property

Obtiene o establece el Nombre del[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición.

BuildingBlock con este nombre[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) tiene que estar presente en el[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) de lo contrarioInvalidOperationException ocurrira.

```csharp
public string PlaceholderName { get; set; }
```

### Ejemplos

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
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* asamblea [Aspose.Words](../../../)


