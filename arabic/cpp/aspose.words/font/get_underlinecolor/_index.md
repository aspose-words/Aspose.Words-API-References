---
title: "طريقة Aspose::Words::Font::get_UnderlineColor"
linktitle: "get_UnderlineColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_UnderlineColor. يحصل على أو يعيّن لون الخط السفلي المطبق على الخط في C++."
type: docs
weight: 56000
url: /ar/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


يحصل أو يضبط لون الخط السفلي المطبق على الخط.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## أمثلة



يظهر كيفية تكوين نمط ولون الخط السفلي للنص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
