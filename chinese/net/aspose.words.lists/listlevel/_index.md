---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Lists.ListLevel 班级. 定义列表级别的格式 在 C#.
type: docs
weight: 3500
url: /zh/net/aspose.words.lists/listlevel/
---
## ListLevel class

定义列表级别的格式。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class ListLevel
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | 获取或设置列表项实际编号的对齐方式。 |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | 获取此列表级别的自定义数字样式格式。例如：“a、ç、ĝ、...”. |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | 指定用于列表标签的字符格式。 |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | 返回当前列表级别的图片项目符号形状的图像数据。 |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | 如果关卡将所有继承的数字转换为阿拉伯数字，则为 true；如果保留其数字样式，则为 false。 |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | 获取或设置链接到此列表级别的段落样式。 |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | 返回或设置列表级别的数字格式。 |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | 返回或设置列表级别的数字或项目符号的位置（以磅为单位）。 |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | 返回或设置此列表级别的数字样式。 |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | 设置或返回指定列表级别重新编号之前必须出现的列表级别。 |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | 返回或设置此列表级别的起始编号。 |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | 返回或设置列表级别的制表符位置（以磅为单位）。 |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | 返回或设置列表级别第二行换行文本的位置（以磅为单位）。 |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | 返回或设置在列表级别的数字之后插入的字符。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | 为当前列表级别创建图片项目符号形状。 |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | 删除当前列表级别的图片项目符号。 |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | 与指定的 ListLevel 进行比较。 |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | 计算该对象的哈希码。 |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | 报告的字符串表示形式`ListLevel`列表项的指定index 的对象。参数指定[`NumberStyle`](../../aspose.words/numberstyle/)以及可选格式 string 时使用Custom已指定。 |

## 评论

您不创建此类的对象。创建列表时，会自动创建列表级对象 。您访问`ListLevel`通过 the 的对象[`ListLevelCollection`](../listlevelcollection/)收藏。

使用以下属性`ListLevel`为各个列表级别指定列表formatting 。

## 例子

演示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其列表的前两个级别。
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// 此 NumberFormat 值将创建星形项目符号列表符号。
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// 创建段落并将自定义列表格式的两个列表级别应用到它们。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
