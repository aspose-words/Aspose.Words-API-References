---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words para .NET
description: Descubra la propiedad IStructuredDocumentTag WordOpenXML, acceda a cadenas XML en formato FlatOpc para una mejor gestión e integración de documentos.
type: docs
weight: 150
url: /es/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato.

```csharp
public string WordOpenXML { get; }
```

## Ejemplos

Muestra cómo obtener XML contenido dentro del nodo en el formato FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Ver también

* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
