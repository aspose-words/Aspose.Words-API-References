---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words for .NET
description: StructuredDocumentTag WordOpenXML mülk. Düğümdeki düğümün içerdiği XMLi temsil eden bir dize alır.FlatOpc format C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Örnekler

Düğümde bulunan XML'in FlatOpc biçiminde nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
