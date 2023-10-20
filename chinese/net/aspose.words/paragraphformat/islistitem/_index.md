---
title: ParagraphFormat.IsListItem
linktitle: IsListItem
articleTitle: IsListItem
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat IsListItem 财产. 当段落是项目符号列表或编号列表中的项目时为真 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words/paragraphformat/islistitem/
---
## ParagraphFormat.IsListItem property

当段落是项目符号列表或编号列表中的项目时为真。

```csharp
public bool IsListItem { get; }
```

## 例子

演示如何将一个列表嵌套在另一个列表中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 创建标题的大纲列表。
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// 创建一个编号列表。
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// 组成列表的每个段落都会有这个标志。
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// 创建项目符号列表。
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// 恢复到编号列表。
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// 恢复到大纲列表。
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
