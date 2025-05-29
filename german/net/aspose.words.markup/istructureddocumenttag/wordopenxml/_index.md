---
title: IStructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words für .NET
description: Entdecken Sie die WordOpenXML-Eigenschaft IStructuredDocumentTag und greifen Sie auf XML-Zeichenfolgen im FlatOpc-Format zu, um die Dokumentenverwaltung und -integration zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.markup/istructureddocumenttag/wordopenxml/
---
## IStructuredDocumentTag.WordOpenXML property

Ruft eine Zeichenfolge ab, die das XML darstellt, das im Knoten imFlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Beispiele

Zeigt, wie XML im Knoten im FlatOpc-Format abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Siehe auch

* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
