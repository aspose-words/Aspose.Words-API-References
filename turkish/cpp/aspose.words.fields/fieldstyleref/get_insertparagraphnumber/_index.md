---
title: "Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumber yöntemi"
linktitle: "get_InsertParagraphNumber"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumber yöntemi. Referans alınan paragrafın paragraf numarasının belgede göründüğü gibi tam olarak eklenip eklenmeyeceğini C++'ta alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldstyleref/get_insertparagraphnumber/
---
## FieldStyleRef::get_InsertParagraphNumber method


Referans alınan paragrafın paragraf numarasını belgede göründüğü gibi tam olarak ekleyip eklemeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumber()
```


## Örnekler



STYLEREF alanlarının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Microsoft Word liste şablonu kullanarak bir liste oluşturun.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Bu oluşturulan liste "1.a )" görüntüleyecek.
// Parantezden önceki boşluk bir ayırıcı olmayan karakterdir ve bunu bastırabiliriz.
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000" u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001" u" )");

// Metin ekleyin ve STYLEREF alanlarının referans alacağı paragraf stillerini uygulayın.
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

// Üstbilgiye bir STYLEREF alanı yerleştirin ve belgede ilk "Liste Paragrafı" stilindeki metni gösterin.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Altbilgiye bir STYLEREF alanı yerleştirin ve son metni göstermesini sağlayın.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// Ayrıca listelerin numaralarına referans vermek için STYLEREF alanlarını kullanabiliriz.
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

## Ayrıca Bakınız

* Class [FieldStyleRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
