---
title: UpdatePageNumbers
second_title: Aspose.Words for C++ API Reference
description: Updates the page numbers for items in this table of contents.
type: docs
weight: 495
url: /cpp/aspose.words.fields/fieldtoc/updatepagenumbers/
---
## FieldToc::UpdatePageNumbers method


Updates the page numbers for items in this table of contents.

```cpp
bool Aspose::Words::Fields::FieldToc::UpdatePageNumbers()
```


### ReturnValue

**true** if the operation is successful. If any of the related TOC bookmarks was removed, **false** will be returned.

## Examples



Shows how to insert a TOC, and populate it with entries based on heading styles. 
```cpp
void FieldToc_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->StartBookmark(u"MyBookmark");

    // Insert a TOC field, which will compile all headings into a table of contents.
    // For each heading, this field will create a line with the text in that heading style to the left,
    // and the page the heading appears on to the right.
    auto field = System::DynamicCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

    // Use the BookmarkName property to only list headings
    // that appear within the bounds of a bookmark with the "MyBookmark" name.
    field->set_BookmarkName(u"MyBookmark");

    // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
    // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
    field->set_CustomStyles(u"Quote; 6; Intense Quote; 7");

    // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
    // but we can set a custom delimiter in this property.
    doc->get_FieldOptions()->set_CustomTocStyleSeparator(u";");

    // Configure the field to exclude any headings that have TOC levels outside of this range.
    field->set_HeadingLevelRange(u"1-3");

    // The TOC will not display the page numbers of headings whose TOC levels are within this range.
    field->set_PageNumberOmittingLevelRange(u"2-5");

    // Set a custom string that will separate every heading from its page number.
    field->set_EntrySeparator(u"-");
    field->set_InsertHyperlinks(true);
    field->set_HideInWebLayout(false);
    field->set_PreserveLineBreaks(true);
    field->set_PreserveTabs(true);
    field->set_UseParagraphOutlineLevel(false);

    InsertNewPageWithHeading(builder, u"First entry", u"Heading 1");
    builder->Writeln(u"Paragraph text.");
    InsertNewPageWithHeading(builder, u"Second entry", u"Heading 1");
    InsertNewPageWithHeading(builder, u"Third entry", u"Quote");
    InsertNewPageWithHeading(builder, u"Fourth entry", u"Intense Quote");

    // These two headings will have the page numbers omitted because they are within the "2-5" range.
    InsertNewPageWithHeading(builder, u"Fifth entry", u"Heading 2");
    InsertNewPageWithHeading(builder, u"Sixth entry", u"Heading 3");

    // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
    InsertNewPageWithHeading(builder, u"Seventh entry", u"Heading 4");

    builder->EndBookmark(u"MyBookmark");
    builder->Writeln(u"Paragraph text.");

    // This entry does not appear because it is outside the bookmark specified by the TOC.
    InsertNewPageWithHeading(builder, u"Eighth entry", u"Heading 1");

    ASSERT_EQ(u" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field->GetFieldCode());

    field->UpdatePageNumbers();
    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.TOC.docx");
}

void InsertNewPageWithHeading(SharedPtr<DocumentBuilder> builder, String captionText, String styleName)
{
    builder->InsertBreak(BreakType::PageBreak);
    String originalStyle = builder->get_ParagraphFormat()->get_StyleName();
    builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(styleName));
    builder->Writeln(captionText);
    builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(originalStyle));
}
```

## See Also

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
