---
title: get_InsertHyperlink
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to insert a hyperlink to the bookmarked paragraph.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldpageref/get_inserthyperlink/
---
## FieldPageRef::get_InsertHyperlink method


Gets or sets whether to insert a hyperlink to the bookmarked paragraph.

```cpp
bool Aspose::Words::Fields::FieldPageRef::get_InsertHyperlink()
```


## Examples



Shows to insert PAGEREF fields to display the relative location of bookmarks. 
```cpp
void FieldPageRef_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    InsertAndNameBookmark(builder, u"MyBookmark1");

    // Insert a PAGEREF field that displays what page a bookmark is on.
    // Set the InsertHyperlink flag to make the field also function as a clickable link to the bookmark.
    ASSERT_EQ(u" PAGEREF  MyBookmark3 \\h", InsertFieldPageRef(builder, u"MyBookmark3", true, false, u"Hyperlink to Bookmark3, on page: ")->GetFieldCode());

    // We can use the \p flag to get the PAGEREF field to display
    // the bookmark's position relative to the position of the field.
    // Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
    ASSERT_EQ(u" PAGEREF  MyBookmark1 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark1", true, true, u"Bookmark1 is ")->GetFieldCode());

    // Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
    ASSERT_EQ(u" PAGEREF  MyBookmark2 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark2", true, true, u"Bookmark2 is ")->GetFieldCode());

    // Bookmark3 will be on a different page, so the field will display "on page 2".
    ASSERT_EQ(u" PAGEREF  MyBookmark3 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark3", true, true, u"Bookmark3 is ")->GetFieldCode());

    InsertAndNameBookmark(builder, u"MyBookmark2");
    builder->InsertBreak(BreakType::PageBreak);
    InsertAndNameBookmark(builder, u"MyBookmark3");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.PAGEREF.docx");
}

static SharedPtr<FieldPageRef> InsertFieldPageRef(SharedPtr<DocumentBuilder> builder, String bookmarkName, bool insertHyperlink,
                                                  bool insertRelativePosition, String textBefore)
{
    builder->Write(textBefore);

    auto field = System::DynamicCast<FieldPageRef>(builder->InsertField(FieldType::FieldPageRef, true));
    field->set_BookmarkName(bookmarkName);
    field->set_InsertHyperlink(insertHyperlink);
    field->set_InsertRelativePosition(insertRelativePosition);
    builder->Writeln();

    return field;
}

static void InsertAndNameBookmark(SharedPtr<DocumentBuilder> builder, String bookmarkName)
{
    builder->StartBookmark(bookmarkName);
    builder->Writeln(String::Format(u"Contents of bookmark \"{0}\".", bookmarkName));
    builder->EndBookmark(bookmarkName);
}
```

## See Also

* Class [FieldPageRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
