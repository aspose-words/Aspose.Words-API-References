---
title: "Aspose::Words::Document::CopyStylesFromTemplate yöntemi"
linktitle: "CopyStylesFromTemplate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::CopyStylesFromTemplate yöntemi. Belirtilen şablondan bir belgeye stilleri C++'da kopyalar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Belirtilen şablondan bir belgeye stilleri kopyalar.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Örnekler



Şablondan bir belgeye stilleri [Document](../) aracılığıyla nasıl kopyalayacağınızı gösterir.
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Bir belgeden diğerine stilleri nasıl kopyalayacağınızı gösterir.
```cpp
// Bir belge oluşturun ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyin.
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

// Stilleri kopyalayacağımız bir belge oluşturun.
auto target = System::MakeObject<Aspose::Words::Document>();

// Şablon belgedeki bir stil ile aynı ada sahip bir stil oluşturun ve hedef belgeye ekleyin.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Bir belgeden diğerine tüm stilleri kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 -  Şablon belge nesnesini geçirme:
target->CopyStylesFromTemplate(template_);

// Stilleri kopyalamak, şablon belgeden tüm stilleri hedefe ekler
// ve aynı ada sahip mevcut stillerin üzerine yazar.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Şablon belgenin yerel sistem dosya adını geçirme:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Ayrıca Bakınız

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Belirtilen şablondan bir belgeye stilleri kopyalar.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Örnekler



Bir belgeden diğerine stilleri nasıl kopyalayacağınızı gösterir.
```cpp
// Bir belge oluşturun ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyin.
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

// Stilleri kopyalayacağımız bir belge oluşturun.
auto target = System::MakeObject<Aspose::Words::Document>();

// Şablon belgedeki bir stil ile aynı ada sahip bir stil oluşturun ve hedef belgeye ekleyin.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// Bir belgeden diğerine tüm stilleri kopyalamak için yöntemi çağırmanın iki yolu vardır.
// 1 -  Şablon belge nesnesini geçirme:
target->CopyStylesFromTemplate(template_);

// Stilleri kopyalamak, şablon belgeden tüm stilleri hedefe ekler
// ve aynı ada sahip mevcut stillerin üzerine yazar.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Şablon belgenin yerel sistem dosya adını geçirme:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
