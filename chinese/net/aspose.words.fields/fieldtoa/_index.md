---
title: FieldToa
second_title: Aspose.Words for .NET API 参考
description: 实现 TOA 字段
type: docs
weight: 2370
url: /zh/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

实现 TOA 字段。

```csharp
public class FieldToa : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldToa](fieldtoa)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname) { get; set; } | 获取或设置书签的名称，该书签标记了用于构建表格的文档部分。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取代表字段end的节点。 |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory) { get; set; } | 获取或设置表中包含的条目的整数类别。 |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator) { get; set; } | 获取或设置用于分隔权限表条目及其页码的字符序列。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 得到一个[`FieldFormat`](../fieldformat)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的LCID。 |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator) { get; set; } | 获取或设置用于分隔页码列表中两个页码的字符序列。 |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator) { get; set; } | 获取或设置用于分隔页面范围的开始和结束的字符序列。 |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting) { get; set; } | 获取或设置是否从权限表中的 条目中删除文档中条目文本的格式。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename) { get; set; } | 获取或设置一个序列的名称，其编号包含在页码中。 |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator) { get; set; } | 获取或设置用于分隔序号和页码的字符序列。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading) { get; set; } | 获取或设置是否在权限表中包含条目的类别标题。 |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim) { get; set; } | 获取或设置是否将五个或多个不同的页面引用替换为相同的 权限为“passim”，用于表示一个单词或段落在被引用的作品中经常出现 。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

使用 TA 指定的 条目构建权限表（即法律文件中的引用列表，例如对案例、法规和规则的引用 ，以及引用出现的页码）字段.

### 例子

展示如何使用 TOA 和 TA 字段构建和自定义权限表。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 TOA 字段，这将为文档中的每个 TA 字段创建一个条目，
    // 显示每个条目的长引用和页码。
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // 为我们的表设置条目类别。此 TOA 现在将仅包含 TA 字段
    // 在其 EntryCategory 属性中具有匹配值。
    fieldToa.EntryCategory = "1";

    // 此外，索引 1 处的权限表类别是“案例”，
    // 如果我们将此变量设置为 true，它将显示为我们表格的标题。
    fieldToa.UseHeading = true;

    // 我们可以通过命名一个需要在 TOA 范围内的书签来进一步过滤 TA 字段。
    fieldToa.BookmarkName = "MyBookmark";

    // 默认情况下，TA 字段的引用之间会出现一个虚线页面范围的选项卡
    // 及其页码。我们可以用我们放在这个属性上的任何文本来替换它。
    // 插入制表符将保留原始制表符。
    fieldToa.EntrySeparator = " \t p.";

    // 如果我们有多个 TA 条目共享相同的长引用，
    // 它们各自的所有页码都将显示在一行上。
    // 我们可以使用这个属性来指定一个字符串来分隔它们的页码。
    fieldToa.PageNumberListSeparator = " & p. ";

    // 我们可以将其设置为 true 以让我们的表格显示单词“passim”
    // 如果一行中有五个或更多页码。
    fieldToa.UsePassim = true;

    // 一个 TA 字段可以引用一系列页面。
    // 我们可以在这里指定一个字符串出现在此类范围的开始页码和结束页码之间。
    fieldToa.PageRangeSeparator = " to ";

    // TA 字段的格式将延续到我们的表格中。
    // 我们可以通过设置 RemoveEntryFormatting 标志来禁用它。
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // 此 TA 字段不会作为条目出现在 TOA 中，因为它在外部
    // TOA 的 BookmarkName 属性指定的书签边界。
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // 这个TA字段在书签里面，
    // 但是条目类别与表格的不匹配，所以TA字段不会包含它。
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // 这个条目将出现在表格中。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // TOA 表不显示短引用，
    // 但我们可以将它们用作速记来引用多个 TA 字段引用的庞大源名称。
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // 我们可以使用以下属性将页码格式化为粗体/斜体。
    // 如果我们将表格设置为忽略格式，我们仍然会看到这些效果。
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // 我们可以配置 TA 字段以获取其 TOA 条目以引用书签跨越的一系列页面。
    // 请注意，此条目与上面的条目引用相同的源以在我们的表中共享一行。
    // 这一行会有上面条目的页码和这个条目的页码范围，
    // 用表格的页列表和页码范围分隔页码。
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // 如果我们启用了表的“Passim”功能，则具有 5 个或更多具有相同源的 TA 条目将调用它。
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

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

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
