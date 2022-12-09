---
title: FieldToa
second_title: Aspose.Words for C++ API Reference
description: Implements the TOA field. To learn more, visit the  documentation article.
type: docs
weight: 1340
url: /cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implements the TOA field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryCategory](./get_entrycategory/)() | Gets or sets the integral category for entries included in the table. |
| [get_EntrySeparator](./get_entryseparator/)() | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SequenceName](./get_sequencename/)() | Gets or sets the name of a sequence whose number is included with the page number. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseHeading](./get_useheading/)() | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [get_UsePassim](./get_usepassim/)() | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_BookmarkName](./get_bookmarkname/). |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_EntryCategory](./get_entrycategory/). |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_EntrySeparator](./get_entryseparator/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Setter for [Aspose::Words::Fields::FieldToa::get_RemoveEntryFormatting](./get_removeentryformatting/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldToa::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseHeading](./set_useheading/)(bool) | Setter for [Aspose::Words::Fields::FieldToa::get_UseHeading](./get_useheading/). |
| [set_UsePassim](./set_usepassim/)(bool) | Setter for [Aspose::Words::Fields::FieldToa::get_UsePassim](./get_usepassim/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to build and customize a table of authorities using TOA and TA fields. 
```cpp
void FieldTOA_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Insert a TOA field, which will create an entry for each TA field in the document,
    // displaying long citations and page numbers for each entry.
    auto fieldToa = System::DynamicCast<FieldToa>(builder->InsertField(FieldType::FieldTOA, false));

    // Set the entry category for our table. This TOA will now only include TA fields
    // that have a matching value in their EntryCategory property.
    fieldToa->set_EntryCategory(u"1");

    // Moreover, the Table of Authorities category at index 1 is "Cases",
    // which will show up as our table's title if we set this variable to true.
    fieldToa->set_UseHeading(true);

    // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
    fieldToa->set_BookmarkName(u"MyBookmark");

    // By default, a dotted line page-wide tab appears between the TA field's citation
    // and its page number. We can replace it with any text we put on this property.
    // Inserting a tab character will preserve the original tab.
    fieldToa->set_EntrySeparator(u" \t p.");

    // If we have multiple TA entries that share the same long citation,
    // all their respective page numbers will show up on one row.
    // We can use this property to specify a string that will separate their page numbers.
    fieldToa->set_PageNumberListSeparator(u" & p. ");

    // We can set this to true to get our table to display the word "passim"
    // if there are five or more page numbers in one row.
    fieldToa->set_UsePassim(true);

    // One TA field can refer to a range of pages.
    // We can specify a string here to appear between the start and end page numbers for such ranges.
    fieldToa->set_PageRangeSeparator(u" to ");

    // The format from the TA fields will carry over into our table.
    // We can disable this by setting the RemoveEntryFormatting flag.
    fieldToa->set_RemoveEntryFormatting(true);
    builder->get_Font()->set_Color(System::Drawing::Color::get_Green());
    builder->get_Font()->set_Name(u"Arial Black");

    ASSERT_EQ(u" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa->GetFieldCode());

    builder->InsertBreak(BreakType::PageBreak);

    // This TA field will not appear as an entry in the TOA since it is outside
    // the bookmark's bounds that the TOA's BookmarkName property specifies.
    SharedPtr<FieldTA> fieldTA = InsertToaEntry(builder, u"1", u"Source 1");

    ASSERT_EQ(u" TA  \\c 1 \\l \"Source 1\"", fieldTA->GetFieldCode());

    // This TA field is inside the bookmark,
    // but the entry category does not match that of the table, so the TA field will not include it.
    builder->StartBookmark(u"MyBookmark");
    fieldTA = InsertToaEntry(builder, u"2", u"Source 2");

    // This entry will appear in the table.
    fieldTA = InsertToaEntry(builder, u"1", u"Source 3");

    // A TOA table does not display short citations,
    // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
    fieldTA->set_ShortCitation(u"S.3");

    ASSERT_EQ(u" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA->GetFieldCode());

    // We can format the page number to make it bold/italic using the following properties.
    // We will still see these effects if we set our table to ignore formatting.
    fieldTA = InsertToaEntry(builder, u"1", u"Source 2");
    fieldTA->set_IsBold(true);
    fieldTA->set_IsItalic(true);

    ASSERT_EQ(u" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA->GetFieldCode());

    // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
    // Note that this entry refers to the same source as the one above to share one row in our table.
    // This row will have the page number of the entry above and the page range of this entry,
    // with the table's page list and page number range separators between page numbers.
    fieldTA = InsertToaEntry(builder, u"1", u"Source 3");
    fieldTA->set_PageRangeBookmarkName(u"MyMultiPageBookmark");

    builder->StartBookmark(u"MyMultiPageBookmark");
    builder->InsertBreak(BreakType::PageBreak);
    builder->InsertBreak(BreakType::PageBreak);
    builder->InsertBreak(BreakType::PageBreak);
    builder->EndBookmark(u"MyMultiPageBookmark");

    ASSERT_EQ(u" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA->GetFieldCode());

    // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, u"1", u"Source 4");
    }

    builder->EndBookmark(u"MyBookmark");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.TOA.TA.docx");
}

static SharedPtr<FieldTA> InsertToaEntry(SharedPtr<DocumentBuilder> builder, String entryCategory, String longCitation)
{
    auto field = System::DynamicCast<FieldTA>(builder->InsertField(FieldType::FieldTOAEntry, false));
    field->set_EntryCategory(entryCategory);
    field->set_LongCitation(longCitation);

    builder->InsertBreak(BreakType::PageBreak);

    return field;
}
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
