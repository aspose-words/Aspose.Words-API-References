---
title: "Aspose::Words::Document::CopyStylesFromTemplate método"
linktitle: "CopyStylesFromTemplate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::CopyStylesFromTemplate método. Copia estilos desde la plantilla especificada a un documento en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Copia estilos de la plantilla especificada a un documento.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Ejemplos



Muestra cómo copiar estilos de la plantilla a un documento a través de [Document](../).
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Muestra cómo copiar estilos de un documento a otro.
```cpp
// Cree un documento y luego añada estilos que copiaremos a otro documento.
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

// Cree un documento al que copiaremos los estilos.
auto target = System::MakeObject<Aspose::Words::Document>();

// Cree un estilo con el mismo nombre que un estilo del documento plantilla y agréguelo al documento de destino.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Hay dos formas de llamar al método para copiar todos los estilos de un documento a otro.
// 1 -  Pasando el objeto del documento plantilla:
target->CopyStylesFromTemplate(template_);

// Copiar estilos agrega todos los estilos del documento plantilla al objetivo
// y sobrescribe los estilos existentes con el mismo nombre.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Pasando el nombre de archivo del sistema local de un documento plantilla:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Ver también

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Copia estilos de la plantilla especificada a un documento.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Ejemplos



Muestra cómo copiar estilos de un documento a otro.
```cpp
// Cree un documento y luego añada estilos que copiaremos a otro documento.
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

// Cree un documento al que copiaremos los estilos.
auto target = System::MakeObject<Aspose::Words::Document>();

// Cree un estilo con el mismo nombre que un estilo del documento plantilla y agréguelo al documento de destino.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Hay dos formas de llamar al método para copiar todos los estilos de un documento a otro.
// 1 -  Pasando el objeto del documento plantilla:
target->CopyStylesFromTemplate(template_);

// Copiar estilos agrega todos los estilos del documento plantilla al objetivo
// y sobrescribe los estilos existentes con el mismo nombre.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Pasando el nombre de archivo del sistema local de un documento plantilla:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
