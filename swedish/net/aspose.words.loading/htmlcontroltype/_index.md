---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words för .NET
description: Upptäck enumereringsprogrammet Aspose.Words.HtmlControlType för sömlös import av HTML-inmatning och markerade element, vilket förbättrar dina dokumentbehandlingsmöjligheter.
type: docs
weight: 4060
url: /sv/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Typ av dokumentnoder som representerar &lt;input&gt;- och &lt;select&gt;-element importerade från HTML.

```csharp
public enum HtmlControlType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| FormField | `0` | Ett formulärfält. |
| StructuredDocumentTag | `1` | En strukturerad dokumenttagg |

## Exempel

Visar hur man anger önskad typ av dokumentnoder som representerar importerade &lt;input&gt;- och &lt;select&gt;-element.

```csharp
const string html = @"
    <html>
        <select name='ComboBox' size='1'>
            <option value='val1'>item1</option>
            <option value='val2'></option>
        </select>
    </html>
";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.PreferredControlType = HtmlControlType.StructuredDocumentTag;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
NodeCollection nodes = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

StructuredDocumentTag tag = (StructuredDocumentTag) nodes[0];
```

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
