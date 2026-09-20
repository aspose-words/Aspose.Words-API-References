---
title: "Метод Aspose::Words::Document::CopyStylesFromTemplate"
linktitle: "CopyStylesFromTemplate"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::CopyStylesFromTemplate. Копирует стили из указанного шаблона в документ в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Копирует стили из указанного шаблона в документ.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Примеры



Показывает, как копировать стили из шаблона в документ через [Document](../).
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Показывает, как копировать стили из одного документа в другой.
```cpp
// Создайте документ, а затем добавьте стили, которые мы скопируем в другой документ.
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

// Создайте документ, в который мы скопируем стили.
auto target = System::MakeObject<Aspose::Words::Document>();

// Создайте стиль с тем же именем, что и стиль из шаблонного документа, и добавьте его в целевой документ.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Существует два способа вызвать метод для копирования всех стилей из одного документа в другой.
// 1 -  Передача объекта шаблонного документа:
target->CopyStylesFromTemplate(template_);

// Копирование стилей добавляет все стили из шаблонного документа в целевой
// и перезаписывает существующие стили с тем же именем.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Передача локального системного имени файла шаблонного документа:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## См. также

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Копирует стили из указанного шаблона в документ.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Примеры



Показывает, как копировать стили из одного документа в другой.
```cpp
// Создайте документ, а затем добавьте стили, которые мы скопируем в другой документ.
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

// Создайте документ, в который мы скопируем стили.
auto target = System::MakeObject<Aspose::Words::Document>();

// Создайте стиль с тем же именем, что и стиль из шаблонного документа, и добавьте его в целевой документ.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Существует два способа вызвать метод для копирования всех стилей из одного документа в другой.
// 1 -  Передача объекта шаблонного документа:
target->CopyStylesFromTemplate(template_);

// Копирование стилей добавляет все стили из шаблонного документа в целевой
// и перезаписывает существующие стили с тем же именем.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Передача локального системного имени файла шаблонного документа:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
