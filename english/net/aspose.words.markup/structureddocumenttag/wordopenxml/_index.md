---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTag WordOpenXML property. Gets a string that represents the XML contained within the node in the FlatOpc format in C#.
type: docs
weight: 300
url: /net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Gets a string that represents the XML contained within the node in the FlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Examples

Shows how to get XML contained within the node in the FlatOpc format.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
