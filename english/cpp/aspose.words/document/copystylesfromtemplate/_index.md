---
title: CopyStylesFromTemplate
second_title: Aspose.Words for C++ API Reference
description: Copies styles from the specified template to a document.
type: docs
weight: 92
url: /cpp/aspose.words/document/copystylesfromtemplate/
---
## Document::CopyStylesFromTemplate(const System::SharedPtr\<Aspose::Words::Document\>\&) method


Copies styles from the specified template to a document.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::SharedPtr<Aspose::Words::Document> &template_)
```


## Examples



Shows how to copies styles from the template to a document via [Document](../). 
```cpp
auto template_ = MakeObject<Document>(MyDir + u"Rendering.docx");
auto target = MakeObject<Document>(MyDir + u"Document.docx");

target->CopyStylesFromTemplate(template_);
```


Shows how to copy styles from one document to another. 
```cpp
// Create a document, and then add styles that we will copy to another document.
auto template_ = MakeObject<Document>();

SharedPtr<Style> style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Create a document which we will copy the styles to.
auto target = MakeObject<Document>();

// Create a style with the same name as a style from the template document and add it to the target document.
style = target->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// There are two ways of calling the method to copy all the styles from one document to another.
// 1 -  Passing the template document object:
target->CopyStylesFromTemplate(template_);

// Copying styles adds all styles from the template document to the target
// and overwrites existing styles with the same name.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Passing the local system filename of a template document:
target->CopyStylesFromTemplate(MyDir + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## See Also

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## Document::CopyStylesFromTemplate(const System::String\&) method


Copies styles from the specified template to a document.

```cpp
void Aspose::Words::Document::CopyStylesFromTemplate(const System::String &template_)
```


## Examples



Shows how to copy styles from one document to another. 
```cpp
// Create a document, and then add styles that we will copy to another document.
auto template_ = MakeObject<Document>();

SharedPtr<Style> style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle1");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle2");
style->get_Font()->set_Name(u"Arial");
style->get_Font()->set_Color(System::Drawing::Color::get_DeepSkyBlue());

style = template_->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Courier New");
style->get_Font()->set_Color(System::Drawing::Color::get_RoyalBlue());

ASSERT_EQ(7, template_->get_Styles()->get_Count());

// Create a document which we will copy the styles to.
auto target = MakeObject<Document>();

// Create a style with the same name as a style from the template document and add it to the target document.
style = target->get_Styles()->Add(StyleType::Paragraph, u"TemplateStyle3");
style->get_Font()->set_Name(u"Calibri");
style->get_Font()->set_Color(System::Drawing::Color::get_Orange());

ASSERT_EQ(5, target->get_Styles()->get_Count());

// There are two ways of calling the method to copy all the styles from one document to another.
// 1 -  Passing the template document object:
target->CopyStylesFromTemplate(template_);

// Copying styles adds all styles from the template document to the target
// and overwrites existing styles with the same name.
ASSERT_EQ(7, target->get_Styles()->get_Count());

ASSERT_EQ(u"Courier New", target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Name());
ASSERT_EQ(System::Drawing::Color::get_RoyalBlue().ToArgb(), target->get_Styles()->idx_get(u"TemplateStyle3")->get_Font()->get_Color().ToArgb());

// 2 -  Passing the local system filename of a template document:
target->CopyStylesFromTemplate(MyDir + u"Rendering.docx");

ASSERT_EQ(21, target->get_Styles()->get_Count());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
