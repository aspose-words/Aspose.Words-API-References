---
title: "Aspose::Words::Document::CopyStylesFromTemplate‑metod"
linktitle: "CopyStylesFromTemplate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::CopyStylesFromTemplate‑metod. Kopierar stilar från den angivna mallen till ett dokument i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Kopierar stilar från den angivna mallen till ett dokument.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Exempel



Visar hur man kopierar stilar från mallen till ett dokument via [Document](../).
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Visar hur man kopierar format från ett dokument till ett annat.
```cpp
// Skapa ett dokument och lägg sedan till format som vi kommer att kopiera till ett annat dokument.
auto template_ = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Skapa ett dokument som vi kommer att kopiera formaten till.
auto target = System::MakeObject<Aspose::Words::Document>();

// Skapa ett format med samma namn som ett format från mall‑dokumentet och lägg till det i mål‑dokumentet.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Det finns två sätt att anropa metoden för att kopiera alla format från ett dokument till ett annat.
// 1 -  Skicka mall‑dokumentobjektet:
target->CopyStylesFromTemplate(template_);

// Att kopiera format lägger till alla format från mall‑dokumentet till mål‑dokumentet
// och skriver över befintliga format med samma namn.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Skicka det lokala systemfilnamnet för ett mall‑dokument:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Se även

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Kopierar stilar från den angivna mallen till ett dokument.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Exempel



Visar hur man kopierar format från ett dokument till ett annat.
```cpp
// Skapa ett dokument och lägg sedan till format som vi kommer att kopiera till ett annat dokument.
auto template_ = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Skapa ett dokument som vi kommer att kopiera formaten till.
auto target = System::MakeObject<Aspose::Words::Document>();

// Skapa ett format med samma namn som ett format från mall‑dokumentet och lägg till det i mål‑dokumentet.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Det finns två sätt att anropa metoden för att kopiera alla format från ett dokument till ett annat.
// 1 -  Skicka mall‑dokumentobjektet:
target->CopyStylesFromTemplate(template_);

// Att kopiera format lägger till alla format från mall‑dokumentet till mål‑dokumentet
// och skriver över befintliga format med samma namn.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Skicka det lokala systemfilnamnet för ett mall‑dokument:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
