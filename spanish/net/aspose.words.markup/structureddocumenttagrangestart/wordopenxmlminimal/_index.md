---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words para .NET
description: Descubra la propiedad StructuredDocumentTagRangeStart en WordOpenXMLMinimal. Acceda a una cadena XML optimizada en formato FlatOpc, centrándose únicamente en el contenido.
type: docs
weight: 180
url: /es/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc format. A diferencia del[`WordOpenXML`](../wordopenxml/) propiedad, este método genera un documento simplificado que excluye cualquier parte no relacionada con el contenido.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Ejemplos

Muestra cómo obtener XML mínimo contenido dentro del nodo en el formato FlatOpc.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Ver también

* class [StructuredDocumentTagRangeStart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
