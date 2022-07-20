---
title: Add
second_title: Aspose.Words for .NET API 参考
description: 创建一个新的用户定义样式并将其添加到集合中
type: docs
weight: 60
url: /zh/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

创建一个新的用户定义样式并将其添加到集合中。

```csharp
public Style Add(StyleType type, string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | StyleType | 一个[`StyleType`](../../styletype)指定要创建的样式类型的值。 |
| name | String | 要创建的样式名称区分大小写。 |

### 评论

您可以创建字符、段落或列表样式。

创建列表样式时，会使用默认编号列表格式 (1\a\i) 创建样式。

如果具有此名称的样式已存在，则引发异常。

### 例子

演示如何将样式添加到文档的样式集合。

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";

// 如果我们添加“StyleType.Paragraph”的样式，该集合将应用
// 将其“DefaultParagraphFormat”属性转换为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// 添加一个样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

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

* class [Style](../../style)
* enum [StyleType](../../styletype)
* class [StyleCollection](../../stylecollection)
* 命名空间 [Aspose.Words](../../stylecollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->