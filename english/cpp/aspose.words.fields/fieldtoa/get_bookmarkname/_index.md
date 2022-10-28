---
title: get_BookmarkName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the bookmark that marks the portion of the document used to build the table.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldtoa/get_bookmarkname/
---
## FieldToa.get_BookmarkName method


Gets or sets the name of the bookmark that marks the portion of the document used to build the table.

```cpp
System::String Aspose::Words::Fields::FieldToa::get_BookmarkName()
```


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

