---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTagRangeStart in WordOpenXMLMinimal. Accedi a una stringa XML semplificata in formato FlatOpc, concentrandoti esclusivamente sul contenuto.
type: docs
weight: 180
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc format. A differenza del[`WordOpenXML`](../wordopenxml/) proprietà, questo metodo genera un documento ridotto che esclude tutte le parti non correlate al contenuto.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Esempi

Mostra come ottenere l'XML minimo contenuto nel nodo nel formato FlatOpc.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Guarda anche

* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
