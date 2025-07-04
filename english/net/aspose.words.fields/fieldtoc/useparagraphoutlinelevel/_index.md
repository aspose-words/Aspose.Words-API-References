---
title: FieldToc.UseParagraphOutlineLevel
linktitle: UseParagraphOutlineLevel
articleTitle: UseParagraphOutlineLevel
second_title: Aspose.Words for .NET
description: Discover how to utilize the FieldToc UseParagraphOutlineLevel property to enhance document organization by setting paragraph outline levels effectively.
type: docs
weight: 170
url: /net/aspose.words.fields/fieldtoc/useparagraphoutlinelevel/
---
## FieldToc.UseParagraphOutlineLevel property

Gets or sets whether to use the applied paragraph outline level.

```csharp
public bool UseParagraphOutlineLevel { get; set; }
```

## Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Insert a TOC field, which will compile all headings into a table of contents.
    // For each heading, this field will create a line with the text in that heading style to the left,
    // and the page the heading appears on to the right.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Use the BookmarkName property to only list headings
    // that appear within the bounds of a bookmark with the "MyBookmark" name.
    field.BookmarkName = "MyBookmark";

    // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
    // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
    // but we can set a custom delimiter in this property.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configure the field to exclude any headings that have TOC levels outside of this range.
    field.HeadingLevelRange = "1-3";

    // The TOC will not display the page numbers of headings whose TOC levels are within this range.
    field.PageNumberOmittingLevelRange = "2-5";

    // Set a custom string that will separate every heading from its page number. 
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

    // These two headings will have the page numbers omitted because they are within the "2-5" range.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // This entry does not appear because it is outside the bookmark specified by the TOC.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.That(field.GetFieldCode(), Is.EqualTo(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w"));

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Start a new page and insert a paragraph of a specified style.
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

### See Also

* class [FieldToc](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
