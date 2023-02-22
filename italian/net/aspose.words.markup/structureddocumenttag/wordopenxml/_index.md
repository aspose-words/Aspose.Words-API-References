---
title: StructuredDocumentTag.WordOpenXML
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Ottiene una stringa che rappresenta lXML contenuto allinterno del nodo nel fileFlatOpc formato.
type: docs
weight: 300
url: /it/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Ottiene una stringa che rappresenta l'XML contenuto all'interno del nodo nel fileFlatOpc formato.

```csharp
public string WordOpenXML { get; }
```

### Esempi

Mostra come ottenere XML contenuto all'interno del nodo nel formato FlatOpc.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


