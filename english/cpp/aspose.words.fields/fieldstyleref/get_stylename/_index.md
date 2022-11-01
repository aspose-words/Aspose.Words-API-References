---
title: get_StyleName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the style by which the text to search for is formatted.
type: docs
weight: 66
url: /cpp/aspose.words.fields/fieldstyleref/get_stylename/
---
## FieldStyleRef.get_StyleName method


Gets or sets the name of the style by which the text to search for is formatted.

```cpp
System::String Aspose::Words::Fields::FieldStyleRef::get_StyleName()
```


## Examples




Shows how to use STYLEREF fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a list based using a Microsoft Word list template.
SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Lists::ListTemplate::NumberDefault);

// This generated list will display "1.a )".
// Space before the bracket is a non-delimiter character, which we can suppress.
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000"
                                                     u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001"
                                                     u" )");

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
auto field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Place a STYLEREF field in the footer, and have it display the last text.
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// We can also use STYLEREF fields to reference the list numbers of lists.
builder->Write(u"\nParagraph number: ");
field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::DynamicCast<FieldStyleRef>(builder->InsertField(FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.STYLEREF.docx");
```

