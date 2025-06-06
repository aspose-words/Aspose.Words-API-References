---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: Aspose.Words for .NET
description: 发现 ListFormat ListLevelNumber 属性，轻松管理从 0 到 8 的段落列表级别，以增强文档的组织性和清晰度。
type: docs
weight: 40
url: /zh/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

获取或设置段落的列表级别编号（0 到 8）。

```csharp
public int ListLevelNumber { get; set; }
```

## 评论

在 Word 文档中，列表可能由 1 或 9 个级别组成，编号为 0 到 8。

仅在[`List`](../list/)属性设置为引用有效列表。

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

展示如何创建项目符号列表和编号列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 以下是我们可以使用文档构建器创建的两种类型的列表。
// 1 - 项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（“•”）。
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// 结束项目符号列表。
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - 编号列表：
// 编号列表通过对每个项目进行编号来为其段落创建逻辑顺序。
builder.ListFormat.ApplyNumberDefault();

// 此段落是第一项。编号列表的第一项将以“1.”作为其列表项符号。
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// 调用“ListIndent”方法来增加当前列表级别，
// 这将在第一个列表级别的当前项目处开始一个新的自包含列表，具有更深的缩进。
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// 这是第二级列表的前三个列表项，将维护一个计数
// 与第一级列表的计数无关。根据当前列表格式，
// 它们将有符号“a.”、“b.”和“c.”。
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// 调用“ListOutdent”方法返回上一个列表级别。
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// 这两段将会延续第一级列表的计数。
// 这些物品将有符号“2.”、“3.”。
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// 如果我们将列表级别增加到之前添加项目的级别，
 // 嵌套列表将与前一个列表分开，并且其编号将从头开始。
// 这些列表项将具有“a.”、“b.”、“c.”、“d.”和“e”的符号。
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// 再次减少列表级别。
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// 结束编号列表。
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### 也可以看看

* class [ListFormat](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
