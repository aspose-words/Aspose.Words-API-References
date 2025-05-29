---
title: ListFormat.RemoveNumbers
linktitle: RemoveNumbers
articleTitle: RemoveNumbers
second_title: Aspose.Words for .NET
description: 使用 ListFormat RemoveNumbers 方法轻松地从段落中删除数字或项目符号，将列表级别重置为零以获得干净的格式。
type: docs
weight: 90
url: /zh/net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

从当前段落中删除数字或项目符号，并将列表级别设置为零。

```csharp
public void RemoveNumbers()
```

## 评论

调用此方法相当于设置[`List`](../list/)财产`无效的`。

## 例子

展示如何从某一部分正文的所有段落中删除列表格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);
Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
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
