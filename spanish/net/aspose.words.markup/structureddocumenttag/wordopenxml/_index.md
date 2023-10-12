---
title: StructuredDocumentTag.WordOpenXML
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag propiedad. Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato.
type: docs
weight: 300
url: /es/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Obtiene una cadena que representa el XML contenido dentro del nodo en elFlatOpc formato.

```csharp
public string WordOpenXML { get; }
```

### Ejemplos

Muestra cómo obtener XML contenido dentro del nodo en formato FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)


