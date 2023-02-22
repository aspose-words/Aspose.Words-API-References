---
title: Class ListFormat
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Lists.ListFormat 班级. 允许控制应用于段落的列表格式
type: docs
weight: 3280
url: /zh/net/aspose.words.lists/listformat/
---
## ListFormat class

允许控制应用于段落的列表格式。

```csharp
public class ListFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | 当段落应用了项目符号或编号格式时为真。 |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | 获取或设置该段落所属的列表。 |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | 返回列表级别格式以及应用于当前段落的任何格式覆盖。 |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | 获取或设置段落的列表级别编号（0 到 8）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | 开始一个新的默认项目符号列表并将其应用于段落。 |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | 开始一个新的默认编号列表并将其应用于段落。 |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | 将当前段落的列表级别提高一级。 |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | 将当前段落的列表级别降低一级。 |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | 从当前段落中删除数字或项目符号并将列表级别设置为零。 |

### 评论

Microsoft Word 文档中的段落可以标有项目符号或编号。 当段落标有项目符号或编号时，表示该段落应用了列表格式 。

您不创建对象`ListFormat`直接上课。 你访问`ListFormat`作为 can 具有与之关联的列表格式的另一个对象的属性。目前 can 具有列表格式的对象是：[`Paragraph`](../../aspose.words/paragraph/), [`Style`](../../aspose.words/style/)和[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat`一个[`Paragraph`](../../aspose.words/paragraph/)指定 应用于该特定段落的列表格式和列表级别。

`ListFormat`一个[`Style`](../../aspose.words/style/)（applicable 仅适用于段落样式）允许指定哪些列表格式和列表 level 应用于该特定样式的所有段落。

`ListFormat`一个[`DocumentBuilder`](../../aspose.words/documentbuilder/) 提供对当前光标位置 内的列表格式的访问[`DocumentBuilder`](../../aspose.words/documentbuilder/).

列表格式本身存储在一个[`List`](../list/) 与段落分开存储的对象。列表 objects 存储在一个[`ListCollection`](../listcollection/)收藏。有一个single [`ListCollection`](../listcollection/)收集每[`Document`](../../aspose.words/document/).

这些段落实际上不属于列表。段落 just 通过[`List`](./list/)property 和列表中的特定级别通过[`ListLevelNumber`](./listlevelnumber/)property. 通过设置这两个属性，您可以控制哪些项目符号和编号 is 应用于段落。

### 例子

显示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
// 我们可以通过增加缩进级别来创建嵌套列表。 
// 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 下面是我们可以使用文档构建器创建的两种类型的列表。
// 1 - 编号列表：
// 编号列表通过对每个项目进行编号来为其段落创建逻辑顺序。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// 通过设置“ListLevelNumber”属性，我们可以增加列表层级
// 在当前列表项开始一个自包含的子列表。
// 名为“NumberDefault”的 Microsoft Word 列表模板使用数字为第一个列表级别创建列表级别。
// 更深的列表级别使用字母和小写罗马数字。 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - 项目符号列表：
// 此列表将在每个段落之前应用缩进和项目符号 ("•")。
// 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“列表”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)


