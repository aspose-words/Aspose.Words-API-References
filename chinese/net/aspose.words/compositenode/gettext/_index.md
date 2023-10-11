---
title: CompositeNode.GetText
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 方法. 获取此节点及其所有子节点的文本
type: docs
weight: 130
url: /zh/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

获取此节点及其所有子节点的文本。

```csharp
public override string GetText()
```

### 评论

返回的字符串包括所有控制字符和特殊字符，如中所述[`ControlChar`](../../controlchar/)。

### 例子

显示在节点上调用 GetText 和 ToString 方法之间的区别。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText 将检索可见文本以及字段代码和特殊字符。
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// 如果保存为传递的保存格式，ToString 将为我们提供文档的外观。
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

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

* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


