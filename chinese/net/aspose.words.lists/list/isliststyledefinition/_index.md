---
title: List.IsListStyleDefinition
linktitle: IsListStyleDefinition
articleTitle: IsListStyleDefinition
second_title: Aspose.Words for .NET
description: 了解 List 的 IsListStyleDefinition 属性是否定义了列表样式。立即解锁列表的增强样式选项！
type: docs
weight: 20
url: /zh/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

返回`真的`如果此列表是列表样式的定义。

```csharp
public bool IsListStyleDefinition { get; }
```

## 评论

当此属性`真的`， 这[`Style`](../style/)属性返回此列表定义的列表样式。

通过修改定义列表样式的列表的属性，您可以修改列表样式的 properties 。

作为列表样式定义的列表不能直接应用于paragraphs 以对其进行编号。

## 例子

展示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在一种样式中包含整个列表对象。
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// 更改列表中所有列表级别的外观。
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// 从样式内的列表创建另一个列表。
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// 添加一些我们的列表将格式化的列表项。
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// 根据列表样式创建并应用另一个列表。
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### 也可以看看

* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
