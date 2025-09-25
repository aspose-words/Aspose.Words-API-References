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
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [get_CustomStyles](./get_customstyles/)() | Gets a list of styles other than the built-in heading styles to include in the table of contents. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Gets a string that should match type identifiers of TC fields being included. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Gets a range of levels of the table of contents entries to be included. |
| [get_EntrySeparator](./get_entryseparator/)() | Gets a sequence of characters that separate an entry and its page number. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Gets a range of heading levels to include. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Gets whether to hide tab leader and page numbers in Web layout view. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Gets whether to make the table of contents entries hyperlinks. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Gets a range of levels of the table of contents entries from which to omits page numbers. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Gets whether to preserve newline characters within table entries. |
| [get_PreserveTabs](./get_preservetabs/)() | Gets whether to preserve tab entries within table entries. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Gets or sets the name of the sequence identifier used when building a table of figures. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Gets whether to use the applied paragraph outline level. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Sets a string that should match type identifiers of TC fields being included. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Sets a range of levels of the table of contents entries to be included. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Sets a sequence of characters that separate an entry and its page number. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Sets a range of heading levels to include. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Sets whether to hide tab leader and page numbers in Web layout view. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Sets whether to make the table of contents entries hyperlinks. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Sets a range of levels of the table of contents entries from which to omits page numbers. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Sets whether to preserve newline characters within table entries. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Sets whether to preserve tab entries within table entries. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Sets whether to use the applied paragraph outline level. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Updates the page numbers for items in this table of contents. |

## Examples



Shows how to populate a TOC field with entries using SEQ fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A TOC field can create an entry in its table of contents for each SEQ field found in the document.
// Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

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

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// There are two ways of using SEQ fields to populate this TOC.
// 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
// This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
// Since this field does not belong to the main sequence identified
// by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
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
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
// The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
// so the TOC entry will display "2>3" at its page count.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
