---
title: ControlChar.SpaceChar
linktitle: SpaceChar
articleTitle: SpaceChar
second_title: 用于 .NET 的 Aspose.Words
description: ControlChar SpaceChar 场地. 空格字符char32 在 C#.
type: docs
weight: 260
url: /zh/net/aspose.words/controlchar/spacechar/
---
## ControlChar.SpaceChar field

空格字符：(char)32.

```csharp
public const char SpaceChar;
```

## 例子

演示如何向文档添加各种控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加常规空格。
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// 添加一个 NBSP，这是一个不间断的空格。
// 与常规空格不同，此空格不能在其位置有自动换行符。
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// 添加制表符。
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// 添加换行符。
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// 添加新行并开始新段落。
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// 换行符有两个版本。
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// 回车和换行可以用一个字符一起表示。
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// 添加段落分隔符，这将开始一个新段落。
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// 添加分节符。这不会构成新的部分或段落。
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// 添加分页符。
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// 分页符与分节符的值相同。
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// 插入一个新部分，然后将其列数设置为 2。
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// 我们可以使用控制字符来标记文本移动到下一列的点。
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// 大多数字符都有对应的 char 和 string。
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### 也可以看看

* class [ControlChar](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
