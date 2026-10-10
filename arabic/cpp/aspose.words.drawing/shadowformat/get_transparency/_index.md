---
title: "طريقة Aspose::Words::Drawing::ShadowFormat::get_Transparency"
linktitle: "get_Transparency"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShadowFormat::get_Transparency. تحصل أو تضبط درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0 في C++."
type: docs
weight: 2750
url: /ar/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


يحصل أو يعيّن درجة الشفافية لتأثير الظل كقيمة بين 0.0 (معتم) و 1.0 (شفاف). القيمة الافتراضية هي 0.0.

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## أمثلة



يوضح كيفية تعيين لون مع الشفافية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## انظر أيضًا

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
