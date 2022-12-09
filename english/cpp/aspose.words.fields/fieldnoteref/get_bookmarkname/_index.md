---
title: get_BookmarkName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the bookmark.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldnoteref/get_bookmarkname/
---
## FieldNoteRef::get_BookmarkName method


Gets or sets the name of the bookmark.

```cpp
System::String Aspose::Words::Fields::FieldNoteRef::get_BookmarkName()
```


## Examples



Shows to insert NOTEREF fields, and modify their appearance. 
```cpp
void FieldNoteRef_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Create a bookmark with a footnote that the NOTEREF field will reference.
    InsertBookmarkWithFootnote(builder, u"MyBookmark1", u"Contents of MyBookmark1", u"Footnote from MyBookmark1");

    // This NOTEREF field will display the number of the footnote inside the referenced bookmark.
    // Setting the InsertHyperlink property lets us jump to the bookmark by Ctrl + clicking the field in Microsoft Word.
    ASSERT_EQ(u" NOTEREF  MyBookmark2 \\h",
              InsertFieldNoteRef(builder, u"MyBookmark2", true, false, false, u"Hyperlink to Bookmark2, with footnote number ")->GetFieldCode());

    // When using the \p flag, after the footnote number, the field also displays the bookmark's position relative to the field.
    // Bookmark1 is above this field and contains footnote number 1, so the result will be "1 above" on update.
    ASSERT_EQ(u" NOTEREF  MyBookmark1 \\h \\p",
              InsertFieldNoteRef(builder, u"MyBookmark1", true, true, false, u"Bookmark1, with footnote number ")->GetFieldCode());

    // Bookmark2 is below this field and contains footnote number 2, so the field will display "2 below".
    // The \f flag makes the number 2 appear in the same format as the footnote number label in the actual text.
    ASSERT_EQ(u" NOTEREF  MyBookmark2 \\h \\p \\f",
              InsertFieldNoteRef(builder, u"MyBookmark2", true, true, true, u"Bookmark2, with footnote number ")->GetFieldCode());

    builder->InsertBreak(BreakType::PageBreak);
    InsertBookmarkWithFootnote(builder, u"MyBookmark2", u"Contents of MyBookmark2", u"Footnote from MyBookmark2");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.NOTEREF.docx");
}

static SharedPtr<FieldNoteRef> InsertFieldNoteRef(SharedPtr<DocumentBuilder> builder, String bookmarkName, bool insertHyperlink,
                                                  bool insertRelativePosition, bool insertReferenceMark, String textBefore)
{
    builder->Write(textBefore);

    auto field = System::DynamicCast<FieldNoteRef>(builder->InsertField(FieldType::FieldNoteRef, true));
    field->set_BookmarkName(bookmarkName);
    field->set_InsertHyperlink(insertHyperlink);
    field->set_InsertRelativePosition(insertRelativePosition);
    field->set_InsertReferenceMark(insertReferenceMark);
    builder->Writeln();

    return field;
}

static void InsertBookmarkWithFootnote(SharedPtr<DocumentBuilder> builder, String bookmarkName, String bookmarkText, String footnoteText)
{
    builder->StartBookmark(bookmarkName);
    builder->Write(bookmarkText);
    builder->InsertFootnote(FootnoteType::Footnote, footnoteText);
    builder->EndBookmark(bookmarkName);
    builder->Writeln();
}
```

## See Also

* Class [FieldNoteRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
