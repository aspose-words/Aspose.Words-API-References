---
title: Class FieldToc
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldToc 班级. 实现 TOC 字段
type: docs
weight: 2530
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
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | 获取或设置书签的名称，该书签标记用于构建表的文档部分。 |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | 获取或设置在构建不包含标题的 标签和编号的图表时使用的序列标识符的名称。 |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | 获取或设置要包含在目录中的内置标题样式以外的样式列表。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | 获取或设置应与所包含的 TC 字段的类型标识符匹配的字符串。 |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | 获取或设置要包含的目录条目的级别范围。 |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | 获取或设置分隔条目及其页码的字符序列。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | 获取或设置要包含的标题级别范围。 |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | 获取或设置是否在 Web 布局视图中隐藏制表符前导符和页码。 |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | 获取或设置是否使目录条目成为超链接。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | 获取或设置要忽略页码的目录条目的级别范围。 |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | 获取或设置应将前缀添加到条目页码的序列的标识符。 |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | 获取或设置是否在表条目中保留换行符。 |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | 获取或设置是否保留表条目中的制表符条目。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | 获取或设置用于分隔序列号和页码的字符序列。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | 获取或设置构建图表表格时使用的序列标识符的名称。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | 获取或设置是否使用应用的段落大纲级别。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(bool) | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | 更新此目录中项目的页码。 |

### 评论

使用 TC 字段指定的条目、 标题级别和指定样式构建目录（也可以是图表），并将该表插入文档中的此位置。

### 例子

演示如何插入目录，并使用基于标题样式的条目填充它。

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // 插入一个 TOC 字段，它将把所有标题编译到目录中。
    // 对于每个标题，此字段将创建一行，左侧包含该标题样式的文本，
    // 标题出现在右侧的页面。
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // 使用 BookmarkName 属性仅列出标题
    // 出现在名称为“MyBookmark”的书签范围内。
    field.BookmarkName = "MyBookmark";

    // 应用了内置标题样式（例如“标题 1”）的文本将被视为标题。
    // 我们可以命名其他样式，以供此属性中的目录及其目录级别选择作为标题。
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // 默认情况下，样式/目录级别在 CustomStyles 属性中用逗号分隔，
    // 但我们可以在此属性中设置自定义分隔符。
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // 配置该字段以排除 TOC 级别超出此范围的任何标题。
    field.HeadingLevelRange = "1-3";

    // TOC不会显示TOC级别在此范围内的标题的页码。
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

    // 该条目不会出现，因为“标题 4”超出了我们之前设置的“1-3”范围。
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // 该条目不会出现，因为它位于目录指定的书签之外。
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// 开始一个新页面，插入指定样式的段落。
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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


