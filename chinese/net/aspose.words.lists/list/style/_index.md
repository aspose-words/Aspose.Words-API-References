---
title: List.Style
second_title: Aspose.Words for .NET API 参考
description: List 财产. 获取此列表引用或定义的列表样式
type: docs
weight: 80
url: /zh/net/aspose.words.lists/list/style/
---
## List.Style property

获取此列表引用或定义的列表样式。

```csharp
public Style Style { get; }
```

### 评论

如果此列表未与列表样式关联，则该属性将返回 null。

列表可以是对列表样式的引用，在这种情况下[`IsListStyleReference`](../isliststylereference/) 将是真的。

列表可以是列表样式的定义，在这种情况下[`IsListStyleDefinition`](../isliststyledefinition/) 将是真的。这样的列表不能直接应用于文档中的段落。

### 例子

展示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
// 我们可以通过增加缩进级别来创建嵌套列表。 
// 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在一个样式中包含一个完整的 List 对象。
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

// 从样式中的列表创建另一个列表。
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// 添加我们的列表将格式化的一些列表项。
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
* 命名空间 [Aspose.Words.Lists](../../list/)
* 部件 [Aspose.Words](../../../)


