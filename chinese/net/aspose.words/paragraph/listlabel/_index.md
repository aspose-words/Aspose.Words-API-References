---
title: Paragraph.ListLabel
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 获得ListLabel提供对此段落的列表编号值和格式 的访问的对象
type: docs
weight: 160
url: /zh/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

获得`ListLabel`提供对此段落的列表编号值和格式 的访问的对象。

```csharp
public ListLabel ListLabel { get; }
```

### 例子

演示如何提取属于列表项的所有段落的列表标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// 查找是否有段落列表。在我们的文档中，我们的列表使用简单的阿拉伯数字，
// 从三点开始到六点结束。
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // 这是我们把这个节点输出为文本格式时获取到的文本。
     // 此文本输出将省略列表标签。修剪任何段落格式字符。
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // 这获取段落在列表当前级别中的位置。如果我们有一个包含多个级别的列表，
    // 这将告诉我们它在该级别上的位置。
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // 将它们组合在一起以在输出中包含列表标签和文本。
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### 也可以看看

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


