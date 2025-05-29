---
title: ListLabel.LabelString
linktitle: LabelString
articleTitle: LabelString
second_title: Aspose.Words for .NET
description: 发现 ListLabel LabelString 属性，可以轻松地以字符串形式表示列表标签，从而轻松增强数据呈现和组织。
type: docs
weight: 20
url: /zh/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

获取列表标签的字符串表示形式。

```csharp
public string LabelString { get; }
```

## 例子

展示如何提取所有列表项段落的列表标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// 查找是否有段落列表。在我们的文档中，列表使用纯阿拉伯数字，
// 从三点开始到六点结束。
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // 这是我们将此节点输出为文本格式时得到的文本。
     // 此文本输出将省略列表标签。请修剪所有段落格式字符。
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // 获取段落在列表当前层级中的位置。如果我们有一个包含多个层的列表，
    // 这将告诉我们它在该级别上的位置。
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // 将它们组合在一起，将列表标签与文本一起包含在输出中。
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### 也可以看看

* class [ListLabel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
