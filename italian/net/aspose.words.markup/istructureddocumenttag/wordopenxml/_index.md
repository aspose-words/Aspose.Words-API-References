---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words per .NET
description: Scopri la proprietà IStructuredDocumentTag WordOpenXML, accedi alle stringhe XML nel formato FlatOpc per una migliore gestione e integrazione dei documenti.
type: docs
weight: 150
url: /it/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

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

* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
