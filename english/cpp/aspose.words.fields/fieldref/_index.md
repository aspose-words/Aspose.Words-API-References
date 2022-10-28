---
title: FieldRef
second_title: Aspose.Words for C++ API Reference
description: Implements the REF field.
type: docs
weight: 1093
url: /cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implements the REF field.

```cpp
class FieldRef : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider, public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets or sets the referenced bookmark's name. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Gets or sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Gets or sets whether to create a hyperlink to the bookmarked paragraph. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Gets or sets whether to insert the relative position of the referenced paragraph. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_NumberSeparator](./get_numberseparator/)() | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be null. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Gets or sets whether to suppress non-delimiter characters. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_IncludeNoteOrComment](./get_includenoteorcomment/). |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_InsertHyperlink](./get_inserthyperlink/). |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_InsertParagraphNumber](./get_insertparagraphnumber/). |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/). |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/). |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_InsertRelativePosition](./get_insertrelativeposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldRef::get_NumberSeparator](./get_numberseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Setter for [Aspose::Words::Fields::FieldRef::get_SuppressNonDelimiters](./get_suppressnondelimiters/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

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


Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Name bookmarked text with a SET field.
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
auto fieldSet = System::DynamicCast<FieldSet>(builder->InsertField(FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
auto fieldRef = System::DynamicCast<FieldRef>(builder->InsertField(FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(ArtifactsDir + u"Field.SET.REF.docx");
```

