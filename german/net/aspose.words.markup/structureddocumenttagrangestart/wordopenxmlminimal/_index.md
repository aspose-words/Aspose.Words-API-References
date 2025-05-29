---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words für .NET
description: Entdecken Sie die StructuredDocumentTagRangeStart-Eigenschaft in WordOpenXMLMinimal. Greifen Sie auf eine optimierte XML-Zeichenfolge im FlatOpc-Format zu und konzentrieren Sie sich ausschließlich auf den Inhalt.
type: docs
weight: 180
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format. Im Gegensatz zu den[`WordOpenXML`](../wordopenxml/) Diese Methode generiert ein abgespecktes Dokument, das alle nicht inhaltsbezogenen Teile ausschließt.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Beispiele

Zeigt, wie man minimales XML erhält, das im Knoten im FlatOpc-Format enthalten ist.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

### Siehe auch

* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
