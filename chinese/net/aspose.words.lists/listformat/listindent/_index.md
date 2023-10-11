---
title: ListFormat.ListIndent
second_title: Aspose.Words for .NET API 参考
description: ListFormat 方法. 将当前段落的列表级别增加一级
type: docs
weight: 70
url: /zh/net/aspose.words.lists/listformat/listindent/
---
## ListFormat.ListIndent method

将当前段落的列表级别增加一级。

```csharp
public void ListIndent()
```

### 评论

此方法更改列表级别并应用新级别的格式设置属性。

在 Word 文档中，列表最多可以包含九个级别。每个级别的列表格式化 指定使用什么项目符号或编号、左缩进、 项目符号和文本之间的空格等。

### 例子

演示如何创建项目符号列表和编号列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 下面是我们可以使用文档生成器创建的两种类型的列表。
// 1 - 项目符号列表：
// 此列表将在每个段落之前应用缩进和项目符号（“•”）。
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

// 本段是第一项。编号列表的第一项将为“1”。作为其列表项符号。
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// 调用“ListIndent”方法增加当前列表级别，
// 这将在第一个列表级别的当前项目处启动一个新的自包含列表，并具有更深的缩进。
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// 这些是第二级列表的前三个列表项，它将维护一个计数
// 与第一个列表级别的计数无关。按照目前的名单格式，
// 它们将具有“a.”、“b.”和“c.”符号。
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// 调用“ListOutdent”方法返回上一级列表。
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// 这两段将继续第一个列表级别的计数。
// 这些项目将具有符号“2.”和“3.”
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// 如果我们将列表级别增加到之前添加项目的级别，
 // 嵌套列表将与前一个列表分开，并且其编号将从头开始。
// 这些列表项将具有“a.”、“b.”、“c.”、“d.”和“e”符号。
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
* 命名空间 [Aspose.Words.Lists](../../listformat/)
* 部件 [Aspose.Words](../../../)


