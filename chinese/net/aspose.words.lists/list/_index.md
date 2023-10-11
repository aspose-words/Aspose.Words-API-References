---
title: Class List
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Lists.List 班级. 表示列表的格式化
type: docs
weight: 3460
url: /zh/net/aspose.words.lists/list/
---
## List class

表示列表的格式化。

要了解更多信息，请访问[使用列表](https://docs.aspose.com/words/net/working-with-lists/)文档文章。

```csharp
public class List : IComparable<List>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | 获取所有者文档。 |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | 返回`真的`如果此列表是列表样式的定义。 |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | 返回`真的`如果此列表是对列表样式的引用。 |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | 返回`真的`当列表包含 9 级时；`错误的`当 1 级时. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | 指定是否应在每个部分重新启动列表。 默认值为`错误的`. |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | 获取列表的唯一标识符。 |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | 获取此列表的列表级别的集合。 |
| [Style](../../aspose.words.lists/list/style/) { get; } | 获取此列表引用或定义的列表样式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | 将指定列表与当前列表进行比较。 |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | 将指定对象与当前对象进行比较。 |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | 与指定列表进行比较。 |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) | 确定指定对象的值是否等于当前对象。 |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | 计算此列表对象的哈希码。 |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(List) | 如果当前列表和给定列表是从同一模板创建的，则返回 true。 |

### 评论

Microsoft Word 文档中的列表是一组列表格式属性。 每个列表最多可以有 9 个级别，并且为每个级别单独定义格式属性，例如数字样式、起始值、 缩进、制表符位置等。

A`List`对象总是属于[`ListCollection`](../listcollection/)收藏。

要创建新列表，请使用[`ListCollection`](../listcollection/)收藏。

要修改列表的格式，请使用[`ListLevel`](../listlevel/)在 中找到的对象[`ListLevels`](./listlevels/)收藏。

要应用或删除段落中的列表格式，请使用[`ListFormat`](../listformat/)。

### 例子

演示如何通过复制列表来重新开始列表中的编号。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其第一列表级别。
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
// 创建一个类似的列表而不对原始列表进行更改。
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

展示如何使用列表级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 下面是我们可以使用文档生成器创建的两种类型的列表。
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
// 此列表将在每个段落之前应用缩进和项目符号（“•”）。
// 此列表的更深层次将使用不同的符号，例如“■”和“○”。
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 我们可以通过取消设置“List”标志来禁用列表格式，以不将任何后续段落格式化为列表。
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Lists](../../aspose.words.lists/)
* 部件 [Aspose.Words](../../)


