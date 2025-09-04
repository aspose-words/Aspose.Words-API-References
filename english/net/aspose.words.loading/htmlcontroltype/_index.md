---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.HtmlControlType enum for seamless import of HTML input and select elements, enhancing your document processing capabilities.
type: docs
weight: 4080
url: /net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Type of document nodes that represent &lt;input&gt; and &lt;select&gt; elements imported from HTML.

```csharp
public enum HtmlControlType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FormField | `0` | A form field. |
| StructuredDocumentTag | `1` | A structured document tag |

## Examples

Shows how to set preferred type of document nodes that will represent imported &lt;input&gt; and &lt;select&gt; elements.

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

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
