---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Lists.ListFormat 类来控制文档中的列表格式。轻松增强段落样式，提升可读性。
type: docs
weight: 3930
url: /zh/net/aspose.words.lists/listformat/
---
## ListFormat class

允许控制应用于段落的列表格式。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class ListFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | 当段落应用了项目符号或编号格式时为 True。 |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | 获取或设置此段落所属的列表。 |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | 返回列表级别格式以及应用于当前段落的任何格式覆盖。 |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | 获取或设置段落的列表级别编号（0 到 8）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | 开始新的默认项目符号列表并将其应用于段落。 |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | 开始新的默认编号列表并将其应用于段落。 |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | 将当前段落的列表级别增加一级。 |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | 将当前段落的列表级别降低一级。 |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | 从当前段落中删除数字或项目符号，并将列表级别设置为零。 |

## 评论

Microsoft Word 文档中的段落可以添加项目符号或编号。 当段落添加项目符号或编号时，即表示将列表格式 应用于该段落。

您无需创建`ListFormat`直接上课。 您访问`ListFormat`作为 can 具有列表格式关联的另一个对象的属性。目前，can 具有列表格式的对象包括：[`Paragraph`](../../aspose.words/paragraph/), [`Style`](../../aspose.words/style/)和[`DocumentBuilder`](../../aspose.words/documentbuilder/)。

`ListFormat`的[`Paragraph`](../../aspose.words/paragraph/)指定 哪种列表格式和列表级别应用于该特定段落。

`ListFormat`的[`Style`](../../aspose.words/style/) （仅适用于段落样式）允许指定哪些列表格式和列表级别应用于该特定样式的所有段落。

`ListFormat`的[`DocumentBuilder`](../../aspose.words/documentbuilder/) 提供对当前光标位置的列表格式的访问 内部[`DocumentBuilder`](../../aspose.words/documentbuilder/)。

列表格式本身存储在[`List`](../list/) 对象与段落分开存储。列表 objects 存储在[`ListCollection`](../listcollection/)集合。有一个 single [`ListCollection`](../listcollection/)每[`Document`](../../aspose.words/document/)。

这些段落实际上并不属于列表。段落 just 通过[`List`](./list/)property 和列表中的特定级别通过[`ListLevelNumber`](./listlevelnumber/)属性。通过设置这两个属性，您可以控制应用于段落的项目符号和编号。

## 例子

展示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 以下是我们可以使用文档构建器创建的两种类型的列表。
// 1 - 编号列表：
// 编号列表通过对每个项目进行编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// 通过设置“ListLevelNumber”属性，我们可以增加列表级别
// 在当前列表项处开始一个独立的子列表。
// 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
 // 更深的列表级别使用字母和小写罗马数字。
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - 项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（“•”）。
// 此列表的更深级别将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“列表”标志来禁用列表格式，以免将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)
