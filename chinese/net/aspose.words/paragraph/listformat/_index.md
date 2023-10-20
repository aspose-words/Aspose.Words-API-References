---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph ListFormat 财产. 提供对段落的列表格式属性的访问 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

提供对段落的列表格式属性的访问。

```csharp
public ListFormat ListFormat { get; }
```

## 例子

演示如何输出文档中作为列表项的所有段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### 也可以看看

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
