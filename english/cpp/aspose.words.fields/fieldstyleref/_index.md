---
title: Aspose::Words::Fields::FieldStyleRef class
linktitle: FieldStyleRef
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldStyleRef class. Implements the STYLEREF field. To learn more, visit the Working with Fields documentation article in C++.'
type: docs
weight: 96000
url: /cpp/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class


Implements the STYLEREF field. 
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldStyleRef : public Field,
                      public IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Gets or sets whether to insert the relative position of the referenced paragraph. |
| [get_SearchFromBottom](./get_searchfrombottom/)() | Gets or sets whether to search from the bottom of the current page, rather from the top. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the style by which the text to search for is formatted. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Gets or sets whether to suppress non-delimiter characters. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Sets whether to insert the relative position of the referenced paragraph. |
| [set_SearchFromBottom](./set_searchfrombottom/)(bool) | Sets whether to search from the bottom of the current page, rather from the top. |
| [set_StyleName](./set_stylename/)(const System::String \&) | Sets the name of the style by which the text to search for is formatted. |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Sets whether to suppress non-delimiter characters. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](../field/gettype/)() const override |  |
| [Is](../field/is/)(const System::TypeInfo \&) const override |  |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| static [Type](../field/type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Sets whether the field is locked (should not recalculate its result). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sets the LCID of the field. |
| [set_Result](../field/set_result/)(const System::String \&) | Sets text that is between the field separator and field end. |
## Remarks

 The STYLEREF is used to reference a fragment of text within the document that is formatted with the specified style. 
## Examples


Shows how to use STYLEREF fields.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a list based using a Microsoft Word list template.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Lists::ListTemplate::NumberDefault);

// This generated list will display "1.a )".
// Space before the bracket is a non-delimiter character, which we can suppress.
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000" u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001" u" )");

// Add text and apply paragraph styles that STYLEREF fields will reference.
builder->get_ListFormat()->set_List(list);
builder->get_ListFormat()->ListIndent();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(u"Item 2");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 3");
builder->get_ListFormat()->RemoveNumbers();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Place a STYLEREF field in the header and display the first "List Paragraph"-styled text in the document.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Place a STYLEREF field in the footer, and have it display the last text.
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// We can also use STYLEREF fields to reference the list numbers of lists.
builder->Write(u"\nParagraph number: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.STYLEREF.docx");
```
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
