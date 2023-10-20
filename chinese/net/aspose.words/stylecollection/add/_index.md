---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection Add 方法. 创建新的用户定义样式并将其添加到集合中 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

创建新的用户定义样式并将其添加到集合中。

```csharp
public Style Add(StyleType type, string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | StyleType | A[`StyleType`](../../styletype/)指定要创建的样式类型的值。 |
| name | String | 要创建的样式名称区分大小写。 |

## 评论

您可以创建字符、段落或列表样式。

创建列表样式时，将使用默认编号列表格式 (1 \ a \ i) 创建样式。

如果具有此名称的样式已存在，则引发异常。

## 例子

演示如何将样式添加到文档的样式集合中。

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";
// 如果我们添加“StyleType.Paragraph”的样式，集合将应用以下值
// 将其“DefaultParagraphFormat”属性设置为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// 添加样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

演示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在样式中包含整个 List 对象。
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

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
