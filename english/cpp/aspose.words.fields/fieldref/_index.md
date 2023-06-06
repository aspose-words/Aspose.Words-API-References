---
title: Aspose::Words::Fields::FieldRef class
linktitle: FieldRef
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldRef class. Implements the REF field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 85000
url: /cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Implements the REF field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
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
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Gets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Gets whether to create a hyperlink to the bookmarked paragraph. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Gets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Gets whether to insert the paragraph number of the referenced paragraph in full context. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Gets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Gets whether to insert the relative position of the referenced paragraph. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_NumberSeparator](./get_numberseparator/)() | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Gets whether to suppress non-delimiter characters. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Sets whether to create a hyperlink to the bookmarked paragraph. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Sets whether to insert the relative position of the referenced paragraph. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Sets whether to suppress non-delimiter characters. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Name bookmarked text with a SET field.
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
auto fieldSet = System::ExplicitCast<FieldSet>(builder->InsertField(FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
auto fieldRef = System::ExplicitCast<FieldRef>(builder->InsertField(FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(ArtifactsDir + u"Field.SET.REF.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
