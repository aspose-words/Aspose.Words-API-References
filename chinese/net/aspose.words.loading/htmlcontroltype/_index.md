---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HtmlControlType 枚举，用于无缝导入 HTML 输入和选择元素，增强您的文档处理能力。
type: docs
weight: 4060
url: /zh/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

表示从 HTML 导入的 &lt;input&gt; 和 &lt;select&gt; 元素的文档节点类型。

```csharp
public enum HtmlControlType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| FormField | `0` | 表单字段。 |
| StructuredDocumentTag | `1` | 结构化文档标签 |

## 例子

展示如何设置代表导入的 &lt;input&gt; 和 &lt;select&gt; 元素的首选文档节点类型。

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

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
