---
title: FieldTA.PageRangeBookmarkName
linktitle: PageRangeBookmarkName
articleTitle: PageRangeBookmarkName
second_title: 用于 .NET 的 Aspose.Words
description: FieldTA PageRangeBookmarkName 财产. 获取或设置书签的名称该书签标记作为条目页码插入的页面范围 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldta/pagerangebookmarkname/
---
## FieldTA.PageRangeBookmarkName property

获取或设置书签的名称，该书签标记作为条目页码插入的页面范围。

```csharp
public string PageRangeBookmarkName { get; set; }
```

## 例子

展示如何使用 TOA 和 TA 字段构建和自定义权限表。

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 TOA 字段，这将为文档中的每个 TA 字段创建一个条目，
    // 显示每个条目的长引用和页码。
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // 设置表的条目类别。此 TOA 现在仅包含 TA 字段
    // 在其 EntryCategory 属性中具有匹配值。
    fieldToa.EntryCategory = "1";

    // 此外，索引 1 处的权限表类别是“案例”，
    // 如果我们将此变量设置为 true，它将显示为表格的标题。
    fieldToa.UseHeading = true;

    // 我们可以通过命名它们需要在 TOA 范围内的书签来进一步过滤 TA 字段。
    fieldToa.BookmarkName = "MyBookmark";

    // 默认情况下，TA 字段的引文之间会出现一个虚线全页选项卡
    // 及其页码。我们可以将其替换为我们在此属性上放置的任何文本。
    // 插入制表符将保留原始制表符。
    fieldToa.EntrySeparator = " \t p.";

    // 如果我们有多个 TA 条目共享相同的长引用，
    // 所有它们各自的页码将显示在一行上。
    // 我们可以使用此属性来指定一个字符串来分隔它们的页码。
    fieldToa.PageNumberListSeparator = " & p. ";

    // 我们可以将其设置为 true 以使我们的表格显示单词“passim”
    // 如果一行中有五个或更多页码。
    fieldToa.UsePassim = true;

    // 一个 TA 字段可以引用一系列页面。
    // 我们可以在此处指定一个字符串，使其出现在此类范围的起始页码和结束页码之间。
    fieldToa.PageRangeSeparator = " to ";

    // TA 字段的格式将延续到我们的表中。
    // 我们可以通过设置RemoveEntryFormatting 标志来禁用此功能。
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // 该 TA 字段不会作为 TOA 中的条目出现，因为它位于外部
    // TOA 的 BookmarkName 属性指定的书签范围。
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // 这个 TA 字段在书签内部，
    // 但条目类别与表类别不匹配，因此TA字段不会包含它。
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // 该条目将出现在表中。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // TOA 表不显示短引用，
    // 但我们可以使用它们作为简写来引用多个 TA 字段引用的庞大源名称。
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // 我们可以使用以下属性将页码格式化为粗体/斜体。
    // 如果我们将表格设置为忽略格式，我们仍然会看到这些效果。
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // 我们可以配置 TA 字段以获取其 TOA 条目来引用书签跨越的页面范围。
    // 请注意，此条目引用与上面的条目相同的源，以共享表中的一行。
    // 该行将包含上面条目的页码和该条目的页范围，
    // 用表格的页列表和页码之间的页码范围分隔符。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // 如果我们启用了表的“Passim”功能，则具有相同源的 5 个或更多 TA 条目将调用它。
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

* class [FieldTA](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
