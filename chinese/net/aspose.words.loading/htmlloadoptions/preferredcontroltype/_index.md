---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: 用于 .NET 的 Aspose.Words
description: HtmlLoadOptions PreferredControlType 财产. 获取或设置表示导入的 input 和 select 元素的文档节点的首选类型 默认值为FormField 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

获取或设置表示导入的 &lt;input&gt; 和 &lt;select&gt; 元素的文档节点的首选类型。 默认值为FormField.

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## 评论

请注意，设置此属性并不能保证所有导入的控件都属于指定类型。 如果 HTML 控件无法用首选类型的文档节点表示，Aspose.Words 将使用 兼容的[`HtmlControlType`](../../htmlcontroltype/)对于该控件.

## 例子

演示如何设置表示导入的 &lt;input&gt; 和 &lt;select&gt; 元素的文档节点的首选类型。

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

### 也可以看看

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
