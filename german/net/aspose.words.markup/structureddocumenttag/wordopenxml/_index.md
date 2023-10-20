---
title: StructuredDocumentTag.WordOpenXML
linktitle: WordOpenXML
articleTitle: WordOpenXML
second_title: Aspose.Words für .NET
description: StructuredDocumentTag WordOpenXML eigendom. Ruft eine Zeichenfolge ab die das im Knoten im enthaltene XML darstelltFlatOpc format in C#.
type: docs
weight: 300
url: /de/net/aspose.words.markup/structureddocumenttag/wordopenxml/
---
## StructuredDocumentTag.WordOpenXML property

Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format.

```csharp
public string WordOpenXML { get; }
```

## Beispiele

Zeigt, wie im Knoten enthaltenes XML im FlatOpc-Format abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.True(tags[0].WordOpenXML
    .Contains(
        "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
