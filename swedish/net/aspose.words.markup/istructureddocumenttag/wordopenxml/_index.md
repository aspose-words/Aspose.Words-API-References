---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IStructuredDocumentTag WordOpenXML och få åtkomst till XML-strängar i FlatOpc-format för förbättrad dokumenthantering och integration.
type: docs
weight: 150
url: /sv/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

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

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
