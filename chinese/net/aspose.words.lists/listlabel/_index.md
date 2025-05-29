---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Lists.ListLabel 类，使用可自定义的列表标签属性增强文档格式，以实现更好的控制和呈现。
type: docs
weight: 3940
url: /zh/net/aspose.words.lists/listlabel/
---
## ListLabel class

定义特定于列表标签的属性。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class ListLabel
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | 获取列表标签字体。 |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | 获取列表标签的字符串表示形式。 |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | 获取此标签的数值。 |

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

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
