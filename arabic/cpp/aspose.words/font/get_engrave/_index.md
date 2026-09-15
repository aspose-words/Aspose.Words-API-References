---
title: "طريقة Aspose::Words::Font::get_Engrave"
linktitle: "get_Engrave"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Engrave. صحيح إذا كان الخط مُنسقًا كمنقوش في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/font/get_engrave/
---
## Font::get_Engrave method


صحيح إذا كان الخط مُنسقًا كمنقوش.

```cpp
bool Aspose::Words::Font::get_Engrave()
```


## أمثلة



يُظهر كيفية تطبيق تأثيرات النقش/المنقوش على النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// فيما يلي طريقتان لاستخدام الظلال لتطبيق تأثير ثلاثي الأبعاد على النص.
// 1 -  نقش النص لجعله يبدو كأن الحروف غارقة في الصفحة:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  إبراز النص لجعله يبدو كأن الحروف تبرز من الصفحة:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
