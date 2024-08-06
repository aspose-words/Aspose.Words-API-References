---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words for .NET
description: IStructuredDocumentTag WordOpenXML property. Gets a string that represents the XML contained within the node in the FlatOpc format in C#.
type: docs
weight: 150
url: /net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

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

* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
