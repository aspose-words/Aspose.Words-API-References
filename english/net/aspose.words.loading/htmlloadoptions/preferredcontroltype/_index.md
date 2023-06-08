---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words for .NET
description: HtmlLoadOptions PreferredControlType property. Gets or sets preferred type of document nodes that will represent imported input and select elements. Default value is FormField in C#.
type: docs
weight: 50
url: /net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Gets or sets preferred type of document nodes that will represent imported &lt;input&gt; and &lt;select&gt; elements. Default value is FormField.

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Remarks

Please note that setting this property does not guarantee that all imported controls will be of the specified type. If an HTML control is not representable with document nodes of the preferred type, Aspose.Words will use a compatible [`HtmlControlType`](../../htmlcontroltype/) for that control.

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

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
