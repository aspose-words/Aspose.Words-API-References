---
title: LabelString
second_title: Aspose.Words for .NET API 参考
description: 获取列表标签的字符串表示形式
type: docs
weight: 20
url: /zh/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

获取列表标签的字符串表示形式。

```csharp
public string LabelString { get; }
```

### 例子

演示如何提取作为列表项的所有段落的列表标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// 查找我们是否有段落列表。在我们的文档中，我们的列表使用纯阿拉伯数字，
// 从三点开始，六点结束。
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // 这是我们将此节点输出为文本格式时得到的文本。
    // 此文本输出将省略列表标签。修剪任何段落格式字符。 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // 这将获取段落在列表当前级别中的位置。如果我们有一个包含多个级别的列表，
    // 这将告诉我们它在那个级别上的位置。
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // 将它们组合在一起以在输出中包含列表标签和文本。
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### 也可以看看

* class [ListLabel](../../listlabel)
* 命名空间 [Aspose.Words.Lists](../../listlabel)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->