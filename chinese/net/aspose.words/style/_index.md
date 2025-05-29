---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Style 类，轻松管理自定义和内置样式。轻松精准地增强您的文档格式。
type: docs
weight: 6980
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
| [Aliases](../../aspose.words/style/aliases/) { get; } | 获取此样式的所有别名。如果样式没有别名，则返回空的字符串数组。 |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | 指定此样式是否根据适当的值自动重新定义。 |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | 获取/设置此样式所基于的样式的名称。 |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | 如果此样式是 MS Word 中的内置样式之一，则为真。 |
| [Document](../../aspose.words/style/document/) { get; } | 获取所有者文档。 |
| [Font](../../aspose.words/style/font/) { get; } | 获取样式的字符格式。 |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | 当样式是内置标题样式之一时为真。 |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; set; } | 获取/设置`Style`链接到此样式。如果没有链接样式，则返回空字符串。 |
| [List](../../aspose.words/style/list/) { get; } | 获取定义此列表样式格式的列表。 |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | 提供对段落样式的列表格式属性的访问。 |
| [Locked](../../aspose.words/style/locked/) { get; set; } | 指定此样式是否被锁定。 |
| [Name](../../aspose.words/style/name/) { get; set; } | 获取或设置样式的名称。 |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | 获取/设置自动应用于在用指定样式格式化的段落后插入的新段落的样式名称。 |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | 获取样式的段落格式。 |
| [Priority](../../aspose.words/style/priority/) { get; set; } | 获取/设置表示在“样式”任务窗格中对样式进行排序的优先级的整数值。 |
| [SemiHidden](../../aspose.words/style/semihidden/) { get; set; } | 获取/设置样式是否从样式库和样式任务窗格中隐藏。 |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | 获取内置样式的区域独立样式标识符。 |
| [Styles](../../aspose.words/style/styles/) { get; } | 获取此样式所属的样式集合。 |
| [Type](../../aspose.words/style/type/) { get; } | 获取样式类型（段落或字符）。 |
| [UnhideWhenUsed](../../aspose.words/style/unhidewhenused/) { get; set; } | 获取/设置当前文档中使用的样式是否从样式库和样式任务窗格中取消隐藏。 当使用的样式应显示在样式库中时为 True。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | 与指定样式进行比较。 仅比较内置样式的样式 Istds。 比较中不包含样式默认值。 以递归方式比较基本样式、链接样式和下一段落样式。 |
| [Remove](../../aspose.words/style/remove/)() | 从文档中删除指定的样式。 |

## 例子

展示如何创建和使用具有列表格式的段落样式。

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

// 将段落样式应用到文档构建器的当前段落，然后添加一些文本。
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// 将文档构建器的样式更改为没有列表格式的样式并编写另一个段落。
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

// 将文档中的一种样式应用到文档构建器正在创建的段落。
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// 从文档的样式集合中删除我们的自定义样式。
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// 任何使用已删除样式的文本都会恢复为默认格式。
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
