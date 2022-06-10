---
title: FieldToc
second_title: Aspose.Words for .NET API 参考
description: 实现 TOC 字段
type: docs
weight: 2340
url: /zh/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

实现 TOC 字段。

```csharp
public class FieldToc : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldToc](fieldtoc)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname) { get; set; } | 获取或设置标记用于构建表的文档部分的书签的名称。 |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel) { get; set; } | 获取或设置在构建不包括标题的 标签和数字的图形表时使用的序列标识符的名称。 |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles) { get; set; } | 获取或设置包含在目录中的内置标题样式以外的样式列表。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取表示字段结束的节点。 |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier) { get; set; } | 获取或设置一个字符串，该字符串应与包含的 TC 字段的类型标识符匹配。 |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange) { get; set; } | 获取或设置要包含的目录条目的级别范围。 |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator) { get; set; } | 获取或设置分隔条目及其页码的字符序列。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 获取[`FieldFormat`](../fieldformat)对象，该对象提供对字段格式的类型化访问。 |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange) { get; set; } | 获取或设置要包含的标题级别范围。 |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout) { get; set; } | 获取或设置是否在 Web 布局视图中隐藏制表符前导和页码。 |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks) { get; set; } | 获取或设置是否使目录条目超链接。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的 LCID。 |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange) { get; set; } | 获取或设置目录条目的级别范围，从中省略页码。 |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier) { get; set; } | 获取或设置序列的标识符，为其添加前缀到条目的页码。 |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks) { get; set; } | 获取或设置是否在表条目中保留换行符。 |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs) { get; set; } | 获取或设置是否在表格条目中保留制表符条目。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator) { get; set; } | 获取或设置用于分隔序号和页码的字符序列。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel) { get; set; } | 获取或设置构建图表时使用的序列标识符的名称。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel) { get; set; } | 获取或设置是否使用应用的段落大纲级别。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包含子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子 ，则返回其父段落。如果该字段已被删除，则返回 **null** 。 |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers)() | 更新此目录中项目的页码。 |

### 评论

使用指定的条目构建目录（也可以是图表） TC 字段、 它们的标题级别和指定的样式，并将该表插入到文档中的此位置。

### 例子

显示如何插入目录，并使用基于标题样式的条目填充它。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目都包含包含 SEQ 字段的段落和该字段出现的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一的命名序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 使用“TableOfFiguresLabel”属性为 TOC 命名一个主序列。
// 现在，此 TOC 将仅在“SequenceIdentifier”设置为“MySequence”的 SEQ 字段中创建条目。
fieldToc.TableOfFiguresLabel = "MySequence";

// 我们可以在“PrefixedSequenceIdentifier”属性中命名另一个 SEQ 字段序列。
 // 此前缀序列中的 SEQ 字段不会创建 TOC 条目。
// 从主序列 SEQ 字段创建的每个 TOC 条目现在也将显示
// 前缀序列当前在产生条目的主序列 SEQ 字段中打开。
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// 每个 TOC 条目将立即在左侧显示前缀序列计数
// 主序列 SEQ 字段出现的页码。
// 我们可以指定将出现在这两个数字之间的自定义分隔符。
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// 使用 SEQ 字段填充此 TOC 有两种方法。
// 1 - 插入一个属于 TOC 前缀序列的 SEQ 字段：
// 此字段会将“PrefixSequence”的 SEQ 序列计数加 1。
// 由于该字段不属于识别的主序列
// 通过 TOC 的“TableOfFiguresLabel”属性，它不会作为条目出现。
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - 插入一个属于 TOC 主序列的 SEQ 字段：
// 此 SEQ 字段将在 TOC 中创建一个条目。
// TOC 条目将包含 SEQ 字段所在的段落以及它出现的页码。
// 此条目还将显示前缀序列当前所处的计数，
// 通过 TOC 的 SeqenceSeparator 属性中的值与页码分隔。
// “PrefixSequence”计数为 1，此主序列 SEQ 字段位于第 2 页，
// 分隔符是“>”，所以条目会显示“1>2”。
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// 插入一个页面，将前缀序列前移2，插入一个SEQ字段，之后创建一个TOC条目。
// 前缀序列现在在 2，主序列 SEQ 字段在第 3 页，
// 所以 TOC 条目将在其页数处显示“2>3”。
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

显示如何使用 SEQ 字段使用条目填充 TOC 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目都包含包含 SEQ 字段的段落和该字段出现的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一的命名序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 使用“TableOfFiguresLabel”属性为 TOC 命名一个主序列。
// 现在，此 TOC 将仅在“SequenceIdentifier”设置为“MySequence”的 SEQ 字段中创建条目。
fieldToc.TableOfFiguresLabel = "MySequence";

// 我们可以在“PrefixedSequenceIdentifier”属性中命名另一个 SEQ 字段序列。
 // 此前缀序列中的 SEQ 字段不会创建 TOC 条目。
// 从主序列 SEQ 字段创建的每个 TOC 条目现在也将显示
// 前缀序列当前在产生条目的主序列 SEQ 字段中打开。
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// 每个 TOC 条目将立即在左侧显示前缀序列计数
// 主序列 SEQ 字段出现的页码。
// 我们可以指定将出现在这两个数字之间的自定义分隔符。
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// 使用 SEQ 字段填充此 TOC 有两种方法。
// 1 - 插入一个属于 TOC 前缀序列的 SEQ 字段：
// 此字段会将“PrefixSequence”的 SEQ 序列计数加 1。
// 由于该字段不属于识别的主序列
// 通过 TOC 的“TableOfFiguresLabel”属性，它不会作为条目出现。
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - 插入一个属于 TOC 主序列的 SEQ 字段：
// 此 SEQ 字段将在 TOC 中创建一个条目。
// TOC 条目将包含 SEQ 字段所在的段落以及它出现的页码。
// 此条目还将显示前缀序列当前所处的计数，
// 通过 TOC 的 SeqenceSeparator 属性中的值与页码分隔。
// “PrefixSequence”计数为 1，此主序列 SEQ 字段位于第 2 页，
// 分隔符是“>”，所以条目会显示“1>2”。
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// 插入一个页面，将前缀序列前移2，插入一个SEQ字段，之后创建一个TOC条目。
// 前缀序列现在在 2，主序列 SEQ 字段在第 3 页，
// 所以 TOC 条目将在其页数处显示“2>3”。
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

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
