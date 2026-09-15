---
title: "Aspose::Words::Document::CopyStylesFromTemplate طريقة"
linktitle: "CopyStylesFromTemplate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::CopyStylesFromTemplate طريقة. ينسخ الأنماط من القالب المحدد إلى مستند في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


ينسخ الأنماط من القالب المحدد إلى مستند.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## أمثلة



يظهر كيفية نسخ الأنماط من القالب إلى مستند عبر [Document](../).
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


يظهر كيفية نسخ الأنماط من مستند إلى آخر.
```cpp
// أنشئ مستندًا، ثم أضف الأنماط التي سنقوم بنسخها إلى مستند آخر.
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

// أنشئ مستندًا سننسخ الأنماط إليه.
auto target = System::MakeObject<Aspose::Words::Document>();

// أنشئ نمطًا بنفس اسم نمط من مستند القالب وأضفه إلى المستند الهدف.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// هناك طريقتان لاستدعاء الطريقة لنسخ جميع الأنماط من مستند إلى آخر.
// 1 -  تمرير كائن مستند القالب:
target->CopyStylesFromTemplate(template_);

// نسخ الأنماط يضيف جميع الأنماط من مستند القالب إلى الهدف
// ويستبدل الأنماط الموجودة التي لها نفس الاسم.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  تمرير اسم ملف نظام محلي لمستند القالب:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## انظر أيضًا

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


ينسخ الأنماط من القالب المحدد إلى مستند.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## أمثلة



يظهر كيفية نسخ الأنماط من مستند إلى آخر.
```cpp
// أنشئ مستندًا، ثم أضف الأنماط التي سنقوم بنسخها إلى مستند آخر.
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

// أنشئ مستندًا سننسخ الأنماط إليه.
auto target = System::MakeObject<Aspose::Words::Document>();

// أنشئ نمطًا بنفس اسم نمط من مستند القالب وأضفه إلى المستند الهدف.
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// هناك طريقتان لاستدعاء الطريقة لنسخ جميع الأنماط من مستند إلى آخر.
// 1 -  تمرير كائن مستند القالب:
target->CopyStylesFromTemplate(template_);

// نسخ الأنماط يضيف جميع الأنماط من مستند القالب إلى الهدف
// ويستبدل الأنماط الموجودة التي لها نفس الاسم.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  تمرير اسم ملف نظام محلي لمستند القالب:
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
