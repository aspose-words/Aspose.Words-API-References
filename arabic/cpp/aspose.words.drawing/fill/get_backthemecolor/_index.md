---
title: "Aspose::Words::Drawing::Fill::get_BackThemeColor طريقة"
linktitle: "get_BackThemeColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Fill::get_BackThemeColor طريقة. يحصل على أو يضبط كائن ThemeColor الذي يمثل لون الخلفية للتعبئة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/fill/get_backthemecolor/
---
## Fill::get_BackThemeColor method


يحصل أو يعيّن كائن ThemeColor الذي يمثل لون الخلفية للتعبئة.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_BackThemeColor()
```


## أمثلة



يظهر كيفية تعيين لون السمة للون الشكل في المقدمة/الخلفية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// ملاحظة: لا تستخدم "BackThemeColor" و "BackTintAndShade" لتعبئة الخط.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## انظر أيضًا

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
