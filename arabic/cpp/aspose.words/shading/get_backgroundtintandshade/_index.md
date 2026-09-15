---
title: "طريقة Aspose::Words::Shading::get_BackgroundTintAndShade"
linktitle: "get_BackgroundTintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Shading::get_BackgroundTintAndShade. يحصل على أو يضبط قيمة مزدوجة تُفتح أو تُغمق لون نمط الخلفية في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


يحصل أو يعيّن قيمة مزدوجة تُفتح أو تُغميق لون سمة الخلفية.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## ملاحظات


القيم المسموح بها تقع في النطاق من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة



يظهر كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## انظر أيضًا

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
