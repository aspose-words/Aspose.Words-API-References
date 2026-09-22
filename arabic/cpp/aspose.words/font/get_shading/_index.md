---
title: "طريقة Aspose::Words::Font::get_Shading"
linktitle: "get_Shading"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Shading. يرجع كائن Shading يشير إلى تنسيق التظليل للخط في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


يعيد كائن [التظليل](../../shading/) الذي يشير إلى تنسيق التظليل للخط.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## أمثلة



يظهر كيفية تطبيق التظليل على النص الذي تم إنشاؤه بواسطة منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// طريقة واحدة لجعل النص الذي تم إنشاؤه باستخدام لون الخط الأبيض مرئيًا
// هي تطبيق تأثير تظليل الخلفية.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## انظر أيضًا

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
