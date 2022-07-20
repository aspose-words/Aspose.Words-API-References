---
title: List
second_title: Aspose.Words for .NET API 参考
description: 表示列表的格式
type: docs
weight: 3260
url: /zh/net/aspose.words.lists/list/
---
## List class

表示列表的格式。

```csharp
public class List : IComparable<List>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.lists/list/document) { get; } | 获取所有者文档。 |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition) { get; } | 如果此列表是列表样式的定义，则返回 true。 |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference) { get; } | 如果此列表是对列表样式的引用，则返回 true。 |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel) { get; } | 当列表包含 9 个级别时返回 true； 1 级时为假。 |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection) { get; set; } | 指定是否应在每个部分重新启动列表。 默认值为 **错误的**. |
| [ListId](../../aspose.words.lists/list/listid) { get; } | 获取列表的唯一标识符。 |
| [ListLevels](../../aspose.words.lists/list/listlevels) { get; } | 获取此列表的列表级别集合。 |
| [Style](../../aspose.words.lists/list/style) { get; } | 获取此列表引用或定义的列表样式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto#compareto)(List) | 将指定列表与当前列表进行比较。 |
| [CompareTo](../../aspose.words.lists/list/compareto#compareto_1)(object) | 将指定对象与当前对象进行比较。 |
| [Equals](../../aspose.words.lists/list/equals#equals)(List) | 与指定列表比较。 |
| override [Equals](../../aspose.words.lists/list/equals#equals_1)(object) |  |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode)() | 计算此列表对象的哈希码。 |

### 评论

Microsoft Word 文档中的列表是一组列表格式属性。 每个列表最多可以有 9 个级别，并且为每个级别单独定义格式属性，例如数字样式、起始值、 缩进、制表位置等。

一个[`List`](../list)对象总是属于[`ListCollection`](../listcollection)收藏。

要创建一个新列表，请使用[`ListCollection`](../listcollection)收藏。

要修改列表的格式，请使用[`ListLevel`](../listlevel)在 中找到的对象[`ListLevels`](./listlevels)收藏。

要在段落中应用或删除列表格式，请使用[`ListFormat`](../listformat).

### 例子

显示如何通过复制列表来重新开始列表中的编号。

```csharp
Document doc = new Document();

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
// 我们可以通过增加缩进级别来创建嵌套列表。 
// 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其第一个列表级别。
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// 将我们的列表应用于某些段落。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// 我们可以将现有列表的副本添加到文档的列表集合中
// 创建一个类似的列表而不更改原始列表。
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// 将第二个列表应用于新段落。
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

演示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们用前缀符号和缩进组织和装饰段落集。
// 我们可以通过增加缩进级别来创建嵌套列表。 
// 我们可以使用文档构建器的“ListFormat”属性来开始和结束一个列表。 
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建一个列表，并自定义其前两个列表级别。
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

// 创建段落并将自定义列表格式的两个列表级别应用于它们。
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

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
