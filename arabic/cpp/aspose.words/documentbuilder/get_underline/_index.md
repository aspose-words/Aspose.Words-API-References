---
title: "طريقة Aspose::Words::DocumentBuilder::get_Underline"
linktitle: "get_Underline"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::get_Underline. يحصل على نوع التسطير أو يضبطه للخط الحالي في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


يحصل/يضبط نوع التسطير للخط الحالي.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## أمثلة



يوضح كيفية تنسيق النص الذي يضيفه منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// يقوم المنشئ بتطبيق التنسيق على الفقرة الحالية وأي نص جديد يضيفه لاحقًا.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## انظر أيضًا

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
