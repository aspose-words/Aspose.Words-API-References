---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTagRangeStart i WordOpenXMLMinimal. Få åtkomst till en strömlinjeformad XML-sträng i FlatOpc-format, med fokus enbart på innehåll.
type: docs
weight: 180
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. Till skillnad från[`WordOpenXML`](../wordopenxml/) egenskapen genererar den här metoden ett avskalat dokument som exkluderar alla delar som inte är innehållsrelaterade.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Exempel

Visar hur man hämtar minimal XML i noden i FlatOpc-formatet.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.True(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
Assert.False(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\"));
```

### Se även

* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
