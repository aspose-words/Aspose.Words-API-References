---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words per .NET
description: Scopri la proprietà WordOpenXML StructuredDocumentTag. Accedi ai dati XML in formato FlatOpc per una perfetta integrazione dei documenti e funzionalità avanzate.
type: docs
weight: 300
url: /it/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc formato.

```csharp
public string WordOpenXML { get; }
```

## Esempi

Mostra come ottenere l'XML contenuto nel nodo nel formato FlatOpc.

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
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
