---
title: "Aspose::Words::Document::CopyStylesFromTemplate metodo"
linktitle: "CopyStylesFromTemplate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::CopyStylesFromTemplate metodo. Copia gli stili dal modello specificato a un documento in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Copia gli stili dal modello specificato a un documento.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Esempi



Mostra come copiare gli stili dal modello a un documento tramite [Document](../).
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Mostra come copiare gli stili da un documento a un altro.
```cpp
// Crea un documento, quindi aggiungi gli stili che copieremo in un altro documento.
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

// Crea un documento al quale copieremo gli stili.
auto target = System::MakeObject<Aspose::Words::Document>();

// Crea uno stile con lo stesso nome di uno stile del documento modello e aggiungilo al documento di destinazione.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Esistono due modi per chiamare il metodo per copiare tutti gli stili da un documento a un altro.
// 1 -  Passare l'oggetto documento modello:
target->CopyStylesFromTemplate(template_);

// La copia degli stili aggiunge tutti gli stili dal documento modello al documento di destinazione
// e sovrascrive gli stili esistenti con lo stesso nome.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Passare il nome file locale del documento modello:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Vedi anche

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Copia gli stili dal modello specificato a un documento.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Esempi



Mostra come copiare gli stili da un documento a un altro.
```cpp
// Crea un documento, quindi aggiungi gli stili che copieremo in un altro documento.
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

// Crea un documento al quale copieremo gli stili.
auto target = System::MakeObject<Aspose::Words::Document>();

// Crea uno stile con lo stesso nome di uno stile del documento modello e aggiungilo al documento di destinazione.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Esistono due modi per chiamare il metodo per copiare tutti gli stili da un documento a un altro.
// 1 -  Passare l'oggetto documento modello:
target->CopyStylesFromTemplate(template_);

// La copia degli stili aggiunge tutti gli stili dal documento modello al documento di destinazione
// e sovrascrive gli stili esistenti con lo stesso nome.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Passare il nome file locale del documento modello:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
