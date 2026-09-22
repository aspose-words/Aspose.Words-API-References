---
title: "طريقة Aspose::Words::Shading::get_ForegroundPatternColor"
linktitle: "get_ForegroundPatternColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Shading::get_ForegroundPatternColor. يحصل على أو يضبط اللون الذي يتم تطبيقه على المقدمة لكائن Shading في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/shading/get_foregroundpatterncolor/
---
## Shading::get_ForegroundPatternColor method


يحصل على أو يضبط اللون الذي يتم تطبيقه على المقدمة لكائن [Shading](../).

```cpp
System::Drawing::Color Aspose::Words::Shading::get_ForegroundPatternColor()
```


## أمثلة



يوضح كيفية تزيين النص بالحدود والتظليل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## انظر أيضًا

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
