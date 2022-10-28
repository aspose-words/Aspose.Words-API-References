---
title: get_IncludeNoteOrComment
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldref/get_includenoteorcomment/
---
## FieldRef.get_IncludeNoteOrComment method


Gets or sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.

```cpp
bool Aspose::Words::Fields::FieldRef::get_IncludeNoteOrComment()
```


## Examples




Shows how to insert REF fields to reference bookmarks. 
```cpp
void FieldRef_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->StartBookmark(u"MyBookmark");
    builder->InsertFootnote(FootnoteType::Footnote, u"MyBookmark footnote #1");
    builder->Write(u"Text that will appear in REF field");
    builder->InsertFootnote(FootnoteType::Footnote, u"MyBookmark footnote #2");
    builder->EndBookmark(u"MyBookmark");
    builder->MoveToDocumentStart();

    // We will apply a custom list format, where the amount of angle brackets indicates the list level we are currently at.
    builder->get_ListFormat()->ApplyNumberDefault();
    builder->get_ListFormat()->get_ListLevel()->set_NumberFormat(u"> \x0000");

    // Insert a REF field that will contain the text within our bookmark, act as a hyperlink, and clone the bookmark's footnotes.
    SharedPtr<FieldRef> field = InsertFieldRef(builder, u"MyBookmark", u"", u"\n");
    field->set_IncludeNoteOrComment(true);
    field->set_InsertHyperlink(true);

    ASSERT_EQ(u" REF  MyBookmark \\f \\h", field->GetFieldCode());

    // Insert a REF field, and display whether the referenced bookmark is above or below it.
    field = InsertFieldRef(builder, u"MyBookmark", u"The referenced paragraph is ", u" this field.\n");
    field->set_InsertRelativePosition(true);

    ASSERT_EQ(u" REF  MyBookmark \\p", field->GetFieldCode());

    // Display the list number of the bookmark as it appears in the document.
    field = InsertFieldRef(builder, u"MyBookmark", u"The bookmark's paragraph number is ", u"\n");
    field->set_InsertParagraphNumber(true);

    ASSERT_EQ(u" REF  MyBookmark \\n", field->GetFieldCode());

    // Display the bookmark's list number, but with non-delimiter characters, such as the angle brackets, omitted.
    field = InsertFieldRef(builder, u"MyBookmark", u"The bookmark's paragraph number, non-delimiters suppressed, is ", u"\n");
    field->set_InsertParagraphNumber(true);
    field->set_SuppressNonDelimiters(true);

    ASSERT_EQ(u" REF  MyBookmark \\n \\t", field->GetFieldCode());

    // Move down one list level.
    builder->get_ListFormat()->set_ListLevelNumber(builder->get_ListFormat()->get_ListLevelNumber() + 1);
    builder->get_ListFormat()->get_ListLevel()->set_NumberFormat(u">> \x0001");

    // Display the list number of the bookmark and the numbers of all the list levels above it.
    field = InsertFieldRef(builder, u"MyBookmark", u"The bookmark's full context paragraph number is ", u"\n");
    field->set_InsertParagraphNumberInFullContext(true);

    ASSERT_EQ(u" REF  MyBookmark \\w", field->GetFieldCode());

    builder->InsertBreak(BreakType::PageBreak);

    // Display the list level numbers between this REF field, and the bookmark that it is referencing.
    field = InsertFieldRef(builder, u"MyBookmark", u"The bookmark's relative paragraph number is ", u"\n");
    field->set_InsertParagraphNumberInRelativeContext(true);

    ASSERT_EQ(u" REF  MyBookmark \\r", field->GetFieldCode());

    // At the end of the document, the bookmark will show up as a list item here.
    builder->Writeln(u"List level above bookmark");
    builder->get_ListFormat()->set_ListLevelNumber(builder->get_ListFormat()->get_ListLevelNumber() + 1);
    builder->get_ListFormat()->get_ListLevel()->set_NumberFormat(u">>> \x0002");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.REF.docx");
}

static SharedPtr<FieldRef> InsertFieldRef(SharedPtr<DocumentBuilder> builder, String bookmarkName, String textBefore, String textAfter)
{
    builder->Write(textBefore);
    auto field = System::DynamicCast<FieldRef>(builder->InsertField(FieldType::FieldRef, true));
    field->set_BookmarkName(bookmarkName);
    builder->Write(textAfter);
    return field;
}
```

