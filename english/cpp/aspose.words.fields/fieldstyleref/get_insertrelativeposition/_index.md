---
title: Aspose::Words::Fields::FieldStyleRef::get_InsertRelativePosition method
linktitle: get_InsertRelativePosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldStyleRef::get_InsertRelativePosition method. Gets or sets whether to insert the relative position of the referenced paragraph in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldstyleref/get_insertrelativeposition/
---
## FieldStyleRef::get_InsertRelativePosition method


Gets or sets whether to insert the relative position of the referenced paragraph.

```cpp
bool Aspose::Words::Fields::FieldStyleRef::get_InsertRelativePosition()
```


## Examples



Shows how to use STYLEREF fields. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a list based using a Microsoft Word list template.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

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
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Place a STYLEREF field in the footer, and have it display the last text.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// We can also use STYLEREF fields to reference the list numbers of lists.
builder->Write(u"\nParagraph number: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.STYLEREF.docx");
```

## See Also

* Class [FieldStyleRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
