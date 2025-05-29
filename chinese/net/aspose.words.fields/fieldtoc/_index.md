---
title: FieldToc Class
linktitle: FieldToc
articleTitle: FieldToc
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldToc 类，在文档中无缝创建目录。强大的功能增强您的工作流程！
type: docs
weight: 2940
url: /zh/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

实现 TOC 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldToc : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldToc](fieldtoc/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | 获取或设置标记用于构建表格的文档部分的书签的名称。 |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | 获取或设置构建不包含标题标签和编号的图表时使用的序列标识符的名称。 |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | 获取或设置除内置标题样式之外的要包含在目录中的样式列表。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | 获取或设置应与所包含的 TC 字段的类型标识符匹配的字符串。 |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | 获取或设置要包含的目录条目的级别范围。 |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | 获取或设置分隔条目及其页码的字符序列。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | 获取或设置要包含的标题级别范围。 |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | 获取或设置是否在 Web 布局视图中隐藏制表符前导符和页码。 |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | 获取或设置是否将目录条目设为超链接。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | 获取或设置目录条目的级别范围，从中省略页码。 |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | 获取或设置应在条目页码中添加前缀的序列的标识符。 |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | 获取或设置是否在表格条目中保留换行符。 |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | 获取或设置是否在表格条目中保留选项卡条目。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | 获取或设置用于分隔序列号和页码的字符序列。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | 获取或设置构建图表时使用的序列标识符的名称。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | 获取或设置是否使用应用的段落大纲级别。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | 更新此目录中项目的页码。 |

## 评论

使用 TC 字段指定的条目、 它们的标题级别和指定的样式构建目录（也可以是图表），并将该表插入文档中的此位置。

## 例子

展示如何插入目录，并根据标题样式填充条目。

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // 插入一个 TOC 字段，它将把所有标题编译成目录。
    // 对于每个标题，此字段将在左侧创建一行带有该标题样式的文本，
    // 并且标题出现在右侧的页面。
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // 使用 BookmarkName 属性仅列出标题
    // 出现在名称为“MyBookmark”的书签范围内。
    field.BookmarkName = "MyBookmark";

    // 应用了内置标题样式（例如“标题 1”）的文本将算作标题。
    // 我们可以在此属性及其 TOC 级别中命名要由 TOC 选取为标题的其他样式。
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // 默认情况下，样式/目录级别在 CustomStyles 属性中以逗号分隔，
    // 但我们可以在此属性中设置自定义分隔符。
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // 配置该字段以排除任何目录级别超出此范围的标题。
    field.HeadingLevelRange = "1-3";

    // 目录不会显示目录级别在此范围内的标题的页码。
    field.PageNumberOmittingLevelRange = "2-5";

     // 设置一个自定义字符串，将每个标题与其页码分开。
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // 这两个标题将省略页码，因为它们在“2-5”范围内。
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // 此条目未出现，因为“标题 4”超出了我们之前设置的“1-3”范围。
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // 此条目未出现，因为它超出了目录指定的书签。
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// 开始一个新页面并插入指定样式的段落。
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
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
