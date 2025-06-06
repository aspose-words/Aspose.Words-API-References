---
title: List.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: 探索列表样式属性，高效定义和自定义列表。独特的样式选项助您提升网页设计！
type: docs
weight: 80
url: /zh/net/aspose.words.lists/list/style/
---
## List.Style property

获取此列表引用或定义的列表样式。

```csharp
public Style Style { get; }
```

## 评论

如果此列表未与列表样式关联，则该属性将返回`无效的`。

在这种情况下，列表可以是对列表样式的引用[`IsListStyleReference`](../isliststylereference/) 将是`真的`。

在这种情况下，列表可以是列表样式的定义[`IsListStyleDefinition`](../isliststyledefinition/) 将是`真的`。这样的列表不能直接应用于文档中的段落。

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

* class [Style](../../../aspose.words/style/)
* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
