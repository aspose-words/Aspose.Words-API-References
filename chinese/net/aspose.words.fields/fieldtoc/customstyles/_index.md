---
title: FieldToc.CustomStyles
linktitle: CustomStyles
articleTitle: CustomStyles
second_title: 用于 .NET 的 Aspose.Words
description: FieldToc CustomStyles 财产. 获取或设置要包含在目录中的内置标题样式以外的样式列表 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldtoc/customstyles/
---
## FieldToc.CustomStyles property

获取或设置要包含在目录中的内置标题样式以外的样式列表。

```csharp
public string CustomStyles { get; set; }
```

## 例子

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

### 也可以看看

* class [FieldToc](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
