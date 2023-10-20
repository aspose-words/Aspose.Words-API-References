---
title: FieldToc.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: 用于 .NET 的 Aspose.Words
description: FieldToc SequenceSeparator 财产. 获取或设置用于分隔序列号和页码的字符序列 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.fields/fieldtoc/sequenceseparator/
---
## FieldToc.SequenceSeparator property

获取或设置用于分隔序列号和页码的字符序列。

```csharp
public string SequenceSeparator { get; set; }
```

## 例子

演示如何使用 SEQ 字段用条目填充 TOC 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目都包含包含 SEQ 字段的段落以及该字段出现的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一的命名序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 使用“TableOfFiguresLabel”属性来命名目录的主序列。
// 现在，此目录将仅在 SEQ 字段之外创建条目，并将其“SequenceIdentifier”设置为“MySequence”。
fieldToc.TableOfFiguresLabel = "MySequence";

// 我们可以在“PrefixedSequenceIdentifier”属性中命名另一个SEQ字段序列。
 // 此前缀序列中的 SEQ 字段不会创建 TOC 条目。
// 从主序列 SEQ 字段创建的每个 TOC 条目现在也将显示该计数
// 前缀序列当前位于生成条目的主序列 SEQ 字段中。
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// 每个 TOC 条目将在左侧立即显示前缀序列计数
// 主序列 SEQ 字段出现的页码。
// 我们可以指定出现在这两个数字之间的自定义分隔符。
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// 有两种使用 SEQ 字段填充此目录的方法。
// 1 - 插入属于 TOC 前缀序列的 SEQ 字段：
// 该字段会将“PrefixSequence”的 SEQ 序列计数加 1。
// 由于该字段不属于所识别的主序列
// 通过目录的“TableOfFiguresLabel”属性，它不会显示为条目。
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - 插入属于 TOC 主序列的 SEQ 字段：
// 此 SEQ 字段将在 TOC 中创建一个条目。
// TOC 条目将包含 SEQ 字段所在的段落及其出现的页码。
// 该条目还将显示前缀序列当前所在的计数，
// 通过目录的 SeqenceSeparator 属性中的值与页码分隔。
// “PrefixSequence”计数为 1，该主序列 SEQ 字段位于第 2 页，
// 分隔符为“>”，因此条目将显示“1>2”。
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// 插入一页，将前缀序列前进2，然后插入SEQ字段以创建TOC条目。
// 前缀序列现在在2，主序列SEQ字段在第3页，
// 因此目录条目将在其页数处显示“2>3”。
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### 也可以看看

* class [FieldToc](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
