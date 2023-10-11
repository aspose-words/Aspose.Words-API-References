---
title: List.ListId
second_title: Aspose.Words for .NET API 参考
description: List 财产. 获取列表的唯一标识符
type: docs
weight: 60
url: /zh/net/aspose.words.lists/list/listid/
---
## List.ListId property

获取列表的唯一标识符。

```csharp
public int ListId { get; }
```

### 评论

您通常不需要使用此属性。但如果你使用它，你通常会与 so 结合使用[`GetListByListId`](../../listcollection/getlistbylistid/)方法通过标识符查找 a 列表。

### 例子

演示如何验证列表的所有者文档属性。

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);
Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
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

* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../list/)
* 部件 [Aspose.Words](../../../)


