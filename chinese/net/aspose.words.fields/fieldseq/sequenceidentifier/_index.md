---
title: FieldSeq.SequenceIdentifier
second_title: Aspose.Words for .NET API 参考
description: FieldSeq 财产. 获取或设置分配给要编号的一系列项目的名称
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

获取或设置分配给要编号的一系列项目的名称。

```csharp
public string SequenceIdentifier { get; set; }
```

### 例子

显示使用 SEQ 字段创建编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一的命名序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 插入一个 SEQ 字段，该字段将显示“MySequence”的当前计数值，
// 使用“ResetNumber”属性将其设置为 100 后。
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// 使用另一个 SEQ 字段显示此序列中的下一个数字。
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 插入 1 级标题。
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// 插入同一序列中的另一个 SEQ 字段，并将其配置为将每个标题的计数重置为 1。
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// 上面的标题是 1 级标题，因此该序列的计数重置为 1。
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// 移动到该序列的下一个数字。
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

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

* class [FieldSeq](../)
* 命名空间 [Aspose.Words.Fields](../../fieldseq/)
* 部件 [Aspose.Words](../../../)


