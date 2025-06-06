---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTag WordOpenXML. Få åtkomst till XML-data i FlatOpc-format för sömlös dokumentintegration och förbättrad funktionalitet.
type: docs
weight: 300
url: /sv/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Exempel

Visar hur man hämtar XML i noden i FlatOpc-format.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
