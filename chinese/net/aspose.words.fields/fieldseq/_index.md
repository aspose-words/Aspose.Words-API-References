---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldSeq 类，实现无缝 SEQ 字段。强大的功能和灵活性增强您的文档自动化。
type: docs
weight: 2800
url: /zh/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

实现 SEQ 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldSeq : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldSeq](fieldseq/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | 获取或设置指向文档中其他位置而非当前位置的项目的书签名称。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | 获取或设置是否插入指定项目的下一个序列号。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | 获取或设置一个表示标题级别的整数，以将序列号重置为。 如果数字不存在，则返回 -1。 |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | 获取或设置一个整数，用于重置序列号。如果该数字不存在，则返回 -1。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | 获取或设置分配给要编号的一系列项目的名称。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

按顺序编号文档中的章节、表格、图表和其他用户定义的项目列表。

## 例子

显示使用 SEQ 字段创建的编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 插入一个 SEQ 字段，用于显示“MySequence”的当前计数值，
// 使用“ResetNumber”属性将其设置为 100 之后。
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

// 从同一序列插入另一个 SEQ 字段，并将其配置为在每个标题处将计数重置为 1。
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// 上述标题是 1 级标题，因此该序列的计数重置为 1。
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// 移动到此序列的下一个数字。
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

展示如何组合目录和序列字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目包含包含SEQ字段的段落，
// 以及该字段出现的页面的编号。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// 将此 TOC 字段配置为具有值为“MySequence”的 SequenceIdentifier 属性。
fieldToc.TableOfFiguresLabel = "MySequence";

// 配置此 TOC 字段以仅选取书签范围内的 SEQ 字段
// 名为“TOCBookmark”。
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 插入一个具有与目录匹配的序列标识符的 SEQ 字段
// TableOfFiguresLabel 属性。此字段不会在目录中创建条目，因为它位于目录之外
// 由“BookmarkName”指定的书签边界。
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性相匹配，并且位于书签的范围内。
// 包含此字段的段落将作为条目显示在目录中。
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性不匹配，
// 并且位于书签的范围内。其段落不会作为条目显示在目录中。
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性相匹配，并且位于书签的范围内。
// 此字段还引用了另一个书签。该书签的内容将出现在此 SEQ 字段的 TOC 条目中。
// SEQ 字段本身不会显示该书签的内容。
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// 创建一个书签，其内容将显示在 TOC 条目中，因为上述 SEQ 字段引用了它。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

展示如何使用 SEQ 字段填充 TOC 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目包含含有 SEQ 字段的段落以及该字段出现的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 使用“TableOfFiguresLabel”属性为目录命名一个主序列。
// 现在，此 TOC 将仅创建 SEQ 字段之外的条目，其“SequenceIdentifier”设置为“MySequence”。
fieldToc.TableOfFiguresLabel = "MySequence";

// 我们可以在“PrefixedSequenceIdentifier”属性中命名另一个SEQ字段序列。
 // 此前缀序列中的 SEQ 字段将不会创建 TOC 条目。
// 从主序列 SEQ 字段创建的每个 TOC 条目现在也将显示计数
// 前缀序列当前位于生成条目的主序列 SEQ 字段上。
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// 每个目录条目将在左侧立即显示前缀序列计数
// 主序列 SEQ 字段出现的页码。
// 我们可以指定出现在这两个数字之间的自定义分隔符。
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// 有两种方法可以使用 SEQ 字段来填充此目录。
// 1 - 插入属于 TOC 前缀序列的 SEQ 字段：
// 此字段将使“PrefixSequence”的 SEQ 序列计数增加 1。
// 由于该字段不属于主序列标识
// 通过目录的“TableOfFiguresLabel”属性，它不会作为条目出现。
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - 插入属于 TOC 主序列的 SEQ 字段：
// 此 SEQ 字段将在 TOC 中创建一个条目。
// TOC 条目将包含 SEQ 字段所在的段落以及它出现的页码。
// 此条目还将显示前缀序列当前的计数，
// 通过 TOC 的 SeqenceSeparator 属性中的值与页码分隔开。
//“PrefixSequence”计数为 1，此主序列 SEQ 字段位于第 2 页，
// 分隔符为“>”，因此条目将显示“1>2”。
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// 插入一页，将前缀序列前进 2，然后插入一个 SEQ 字段以随后创建 TOC 条目。
// 前缀序列现在位于 2，主序列 SEQ 字段位于第 3 页，
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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
