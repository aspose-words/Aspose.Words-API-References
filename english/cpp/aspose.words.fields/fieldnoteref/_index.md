---
title: FieldNoteRef
second_title: Aspose.Words for C++ API Reference
description: Implements the NOTEREF field.
type: docs
weight: 924
url: /cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


Implements the NOTEREF field.

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets or sets the name of the bookmark. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Gets or sets whether to insert a hyperlink to the bookmarked paragraph. |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | Inserts the reference mark with the same character formatting as the Footnote Reference or Endnote Reference style. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Gets or sets whether to insert a relative position of the bookmarked paragraph. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldNoteRef::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Setter for [Aspose::Words::Fields::FieldNoteRef::get_InsertHyperlink](./get_inserthyperlink/). |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | Setter for [Aspose::Words::Fields::FieldNoteRef::get_InsertReferenceMark](./get_insertreferencemark/). |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Setter for [Aspose::Words::Fields::FieldNoteRef::get_InsertRelativePosition](./get_insertrelativeposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

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

