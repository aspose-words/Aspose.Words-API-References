---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words for .NET
description: 使用段落 ListLabel 属性访问并格式化列表编号。轻松增强文档的组织性和清晰度！
type: docs
weight: 160
url: /zh/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

获得`ListLabel`提供对列表编号值和此段落的格式 的访问的对象。

```csharp
public ListLabel ListLabel { get; }
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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
