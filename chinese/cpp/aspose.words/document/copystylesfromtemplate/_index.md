---
title: "Aspose::Words::Document::CopyStylesFromTemplate 方法"
linktitle: "CopyStylesFromTemplate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::CopyStylesFromTemplate 方法。将指定模板中的样式复制到 C++ 文档中。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


将指定模板中的样式复制到文档中。

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## 示例



展示如何通过 [Document](../) 将模板中的样式复制到文档。
```cpp
auto template_ = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto target = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


展示如何将样式从一个文档复制到另一个文档。
```cpp
// 创建一个文档，然后添加我们将复制到另一个文档的样式。
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

// 创建一个我们将把样式复制到的文档。
auto target = System::MakeObject<Aspose::Words::Document>();

// 创建一个与模板文档中样式同名的样式，并将其添加到目标文档。
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// 有两种调用该方法以将所有样式从一个文档复制到另一个文档的方式。
// 1 - 传递模板文档对象：
target->CopyStylesFromTemplate(template_);

// 复制样式会将模板文档中的所有样式添加到目标文档
// 并覆盖具有相同名称的现有样式。
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## 另见

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


将指定模板中的样式复制到文档中。

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## 示例



展示如何将样式从一个文档复制到另一个文档。
```cpp
// 创建一个文档，然后添加我们将复制到另一个文档的样式。
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

// 创建一个我们将把样式复制到的文档。
auto target = System::MakeObject<Aspose::Words::Document>();

// 创建一个与模板文档中样式同名的样式，并将其添加到目标文档。
style = target->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// 有两种调用该方法以将所有样式从一个文档复制到另一个文档的方式。
// 1 - 传递模板文档对象：
target->CopyStylesFromTemplate(template_);

// 复制样式会将模板文档中的所有样式添加到目标文档
// 并覆盖具有相同名称的现有样式。
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 - 传递模板文档的本地系统文件名：
target->CopyStylesFromTemplate(get_MyDir() + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
