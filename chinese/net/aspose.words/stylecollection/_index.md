---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.StyleCollection 班级. 的集合Style表示文档中内置样式和用户定义样式的对象 在 C#.
type: docs
weight: 6140
url: /zh/net/aspose.words/stylecollection/
---
## StyleCollection class

的集合[`Style`](../style/)表示文档中内置样式和用户定义样式的对象。

要了解更多信息，请访问[使用样式和主题](https://docs.aspose.com/words/net/working-with-styles-and-themes/)文档文章。

```csharp
public class StyleCollection : IEnumerable<Style>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | 获取集合中的样式数量。 |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | 获取文档默认文本格式。 |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | 获取文档默认段落格式。 |
| [Document](../../aspose.words/stylecollection/document/) { get; } | 获取所有者文档。 |
| [Item](../../aspose.words/stylecollection/item/) { get; } | 通过名称或别名获取样式。 (3 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | 创建新的用户定义样式并将其添加到集合中。 |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | 将样式复制到此集合中。 |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | 从快速样式库面板中删除所有样式。 |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | 获取一个枚举器对象，该对象将按名称的字母顺序枚举样式。 |

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

### 也可以看看

* class [Style](../style/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
