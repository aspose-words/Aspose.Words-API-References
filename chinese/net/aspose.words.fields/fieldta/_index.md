---
title: FieldTA Class
linktitle: FieldTA
articleTitle: FieldTA
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldTA 类，实现无缝 TA 字段实现，增强文档自动化和格式化功能。
type: docs
weight: 2880
url: /zh/net/aspose.words.fields/fieldta/
---
## FieldTA class

实现 TA 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldTA : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldTA](fieldta/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | 获取或设置整数条目类别，该数字对应于类别的顺序。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | 获取或设置是否对条目的页码应用粗体格式。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | 获取或设置是否对条目的页码应用斜体格式。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | 获取或设置条目的长引用。 |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | 获取或设置标记插入为条目页码的页面范围的书签名称。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | 获取或设置条目的简短引用。 |
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

定义授权表条目的文本和页码，供 TOA 字段使用。

## 例子

展示如何使用 TOA 和 TA 字段构建和自定义引文表。

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 TOA 字段，它将为文档中的每个 TA 字段创建一个条目，
    // 显示每个条目的长引用和页码。
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // 设置表格的条目类别。此 TOA 现在将仅包含 TA 字段
    // 在其 EntryCategory 属性中具有匹配的值。
    fieldToa.EntryCategory = "1";

    // 此外，索引 1 处的权威表类别是“案例”，
    // 如果我们将此变量设置为 true，它将显示为我们的表的标题。
    fieldToa.UseHeading = true;

    // 我们可以通过命名书签来进一步过滤 TA 字段，这些书签需要在 TOA 范围内。
    fieldToa.BookmarkName = "MyBookmark";

    // 默认情况下，TA 字段的引用之间会出现一个虚线页面宽度的标签
    // 及其页码。我们可以用我们在此属性上放置的任何文本来替换它。
    // 插入制表符将保留原始制表符。
    fieldToa.EntrySeparator = " \t p.";

    // 如果我们有多个 TA 条目共享相同的长引用，
    // 所有相应的页码将显示在一行上。
    // 我们可以使用此属性来指定一个字符串来分隔它们的页码。
    fieldToa.PageNumberListSeparator = " & p. ";

    // 我们可以将其设置为 true，以使我们的表格显示单词“passim”
    // 如果一行中有五个或更多页码。
    fieldToa.UsePassim = true;

    // 一个TA字段可以引用一系列页面。
    // 我们可以在这里指定一个字符串，使其出现在这些范围的起始页码和结束页码之间。
    fieldToa.PageRangeSeparator = " to ";

    // TA 字段的格式将延续到我们的表中。
    // 我们可以通过设置 RemoveEntryFormatting 标志来禁用此功能。
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // 此 TA 字段不会作为条目出现在 TOA 中，因为它位于
    // TOA 的 BookmarkName 属性指定的书签边界。
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // 此 TA 字段位于书签内，
    // 但条目类别与表的类别不匹配，因此 TA 字段不会包含它。
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // 该条目将出现在表中。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // TOA 表不显示简短的引用，
    // 但我们可以使用它们作为简写来引用多个 TA 字段引用的庞大源名称。
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // 我们可以使用以下属性格式化页码，使其变为粗体/斜体。
    // 如果我们将表设置为忽略格式，我们仍然会看到这些效果。
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // 我们可以配置 TA 字段以获取其 TOA 条目来引用书签跨越的页面范围。
    // 请注意，此条目与上面的条目引用相同的源，以在我们的表中共享一行。
    // 此行将包含上面条目的页码和此条目的页面范围，
    // 表格的页面列表和页码之间的页码范围分隔符。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // 如果我们启用了表的“Passim”功能，则拥有 5 个或更多具有相同来源的 TA 条目将调用它。
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
