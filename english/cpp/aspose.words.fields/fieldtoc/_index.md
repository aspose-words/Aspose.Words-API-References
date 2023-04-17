---
title: Aspose::Words::Fields::FieldToc class
linktitle: FieldToc
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldToc class. Implements the TOC field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 105000
url: /cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implements the TOC field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::ITocEntryExtractorOptions
```

## Methods

| Method | Description |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() override | Gets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [get_CustomStyles](./get_customstyles/)() | Gets or sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Gets or sets a string that should match type identifiers of TC fields being included. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Gets or sets a range of levels of the table of contents entries to be included. |
| [get_EntrySeparator](./get_entryseparator/)() | Gets or sets a sequence of characters that separate an entry and its page number. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Gets or sets a range of heading levels to include. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Gets or sets whether to hide tab leader and page numbers in Web layout view. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Gets or sets whether to make the table of contents entries hyperlinks. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Gets or sets a range of levels of the table of contents entries from which to omits page numbers. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Gets or sets whether to preserve newline characters within table entries. |
| [get_PreserveTabs](./get_preservetabs/)() | Gets or sets whether to preserve tab entries within table entries. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() override | Gets or sets the name of the sequence identifier used when building a table of figures. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() override | Gets or sets whether to use the applied paragraph outline level. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_BookmarkName](./get_bookmarkname/). |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_CustomStyles](./get_customstyles/). |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_EntryIdentifier](./get_entryidentifier/). |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_EntryLevelRange](./get_entrylevelrange/). |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_EntrySeparator](./get_entryseparator/). |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_HeadingLevelRange](./get_headinglevelrange/). |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Setter for [Aspose::Words::Fields::FieldToc::get_HideInWebLayout](./get_hideinweblayout/). |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Setter for [Aspose::Words::Fields::FieldToc::get_InsertHyperlinks](./get_inserthyperlinks/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/). |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Setter for [Aspose::Words::Fields::FieldToc::get_PreserveLineBreaks](./get_preservelinebreaks/). |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Setter for [Aspose::Words::Fields::FieldToc::get_PreserveTabs](./get_preservetabs/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Setter for [Aspose::Words::Fields::FieldToc::get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Updates the page numbers for items in this table of contents. |

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


Shows how to populate a TOC field with entries using SEQ fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A TOC field can create an entry in its table of contents for each SEQ field found in the document.
// Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
auto fieldToc = System::DynamicCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
// Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
// SEQ fields from this prefix sequence will not create TOC entries.
// Every TOC entry created from a main sequence SEQ field will now also display the count that
// the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Each TOC entry will display the prefix sequence count immediately to the left
// of the page number that the main sequence SEQ field appears on.
// We can specify a custom separator that will appear between these two numbers.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(BreakType::PageBreak);

// There are two ways of using SEQ fields to populate this TOC.
// 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
// This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
// Since this field does not belong to the main sequence identified
// by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
auto fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
// This SEQ field will create an entry in the TOC.
// The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
// This entry will also display the count that the prefix sequence is currently at,
// separated from the page number by the value in the TOC's SeqenceSeparator property.
// The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
// and the separator is ">", so entry will display "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
// The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
// so the TOC entry will display "2>3" at its page count.
builder->InsertBreak(BreakType::PageBreak);
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::DynamicCast<FieldSeq>(builder->InsertField(FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.TOC.SEQ.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
