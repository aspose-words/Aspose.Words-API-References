---
title: ControlChar.NonBreakingHyphenChar
linktitle: NonBreakingHyphenChar
articleTitle: NonBreakingHyphenChar
second_title: Aspose.Words for .NET
description: 探索 Microsoft Word 中的 NonBreaking HyphenChar（不间断连字符）。使用 char30 字符，让文档文本流畅流畅，获得专业效果。
type: docs
weight: 160
url: /zh/net/aspose.words/controlchar/nonbreakinghyphenchar/
---
## ControlChar.NonBreakingHyphenChar field

Microsoft Word 中的不间断连字符是 (char)30.

```csharp
public const char NonBreakingHyphenChar;
```

## 评论

Microsoft Word 中的不间断连字符并不对应于 Unicode 字符 U+2011 不间断连字符，而是代表内部信息，告诉 Microsoft Word 显示连字符而不是换行。

有用信息：http://www.cs.tut.fi/~jkorpela/dashes.html#linebreaks。

## 例子

展示如何向文档添加各种控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加常规空格。
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// 添加 NBSP，即不间断空格。
// 与常规空格不同，此空格不能在其位置自动换行。
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

// 回车符和换行符可以用一个字符一起表示。
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// 添加段落分隔符，以开始新的段落。
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// 添加分节符。这不会创建新的节或段落。
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// 添加分页符。
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// 分页符与分节符的值相同。
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// 插入一个新部分，然后将其列数设置为二。
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// 我们可以使用控制字符来标记文本移动到下一列的位置。
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// 大多数字符都有 char 和 string 对应物。
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
