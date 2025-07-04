---
title: StructuredDocumentTagRangeStart.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words for .NET
description: Discover the StructuredDocumentTagRangeStart property in WordOpenXMLMinimal. Access a streamlined XML string in FlatOpc format, focusing solely on content.
type: docs
weight: 180
url: /net/aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart.WordOpenXMLMinimal property

Gets a string that represents the XML contained within the node in the FlatOpc format. Unlike the [`WordOpenXML`](../wordopenxml/) property, this method generates a stripped-down document that excludes any non-content-related parts.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Examples

Shows how to get minimal XML contained within the node in the FlatOpc format.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

Assert.That(tag.WordOpenXMLMinimal
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"), Is.True);
Assert.That(tag.WordOpenXMLMinimal.Contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""), Is.False);
```

### See Also

* class [StructuredDocumentTagRangeStart](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
