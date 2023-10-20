---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Style 班级. 表示单个内置或用户定义的样式 在 C#.
type: docs
weight: 6130
url: /zh/net/aspose.words/style/
---
## Style class

表示单个内置或用户定义的样式。

要了解更多信息，请访问[使用样式和主题](https://docs.aspose.com/words/net/working-with-styles-and-themes/)文档文章。

```csharp
public class Style
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | 获取此样式的所有别名。如果样式没有别名，则返回空字符串数组。 |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | 指定是否根据适当的值自动重新定义此样式。 |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | 获取/设置此样式所基于的样式的名称。 |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | 如果此样式是 MS Word 中的内置样式之一，则为 True。 |
| [Document](../../aspose.words/style/document/) { get; } | 获取所有者文档。 |
| [Font](../../aspose.words/style/font/) { get; } | 获取样式的字符格式。 |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | 当样式是内置标题样式之一时为真。 |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | 获取名称`Style`与此相关。如果没有链接样式，则返回空字符串。 |
| [List](../../aspose.words/style/list/) { get; } | 获取定义此列表样式格式的列表。 |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | 提供对段落样式的列表格式属性的访问。 |
| [Name](../../aspose.words/style/name/) { get; set; } | 获取或设置样式的名称。 |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | 获取/设置要自动应用于在使用指定样式格式化的 a 段落之后插入的新段落的样式名称。 |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | 获取样式的段落格式。 |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | 获取内置样式的独立于区域设置的样式标识符。 |
| [Styles](../../aspose.words/style/styles/) { get; } | 获取该样式所属的样式集合。 |
| [Type](../../aspose.words/style/type/) { get; } | 获取样式类型（段落或字符）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | 与指定样式进行比较。 仅比较内置样式的样式 Istd。 比较中不包括默认样式。 递归比较基本样式、链接样式和下一段样式。 |
| [Remove](../../aspose.words/style/remove/)() | 从文档中删除指定的样式。 |

## 例子

演示如何创建和使用具有列表格式的段落样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建自定义段落样式。
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// 创建一个列表并确保使用此样式的段落将使用此列表。
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// 将段落样式应用到文档生成器的当前段落，然后添加一些文本。
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// 将文档生成器的样式更改为没有列表格式的样式并编写另一段。
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

展示如何创建和应用自定义样式。

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// 自动重新定义样式。
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// 将文档中的一种样式应用到文档生成器正在创建的段落。
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// 从文档的样式集合中删除我们的自定义样式。
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// 使用已删除样式的任何文本都会恢复为默认格式。
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
