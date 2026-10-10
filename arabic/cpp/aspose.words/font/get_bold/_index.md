---
title: "Aspose::Words::Font::get_Bold طريقة"
linktitle: "get_Bold"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Bold طريقة. صحيح إذا تم تنسيق الخط كغامق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


صحيح إذا كان الخط مُنسقًا كغامق.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## أمثلة



يوضح كيفية إدراج نص منسق باستخدام [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد تنسيق الخط، ثم أضف النص.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
