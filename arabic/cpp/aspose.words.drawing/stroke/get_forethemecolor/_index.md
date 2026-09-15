---
title: "طريقة Aspose::Words::Drawing::Stroke::get_ForeThemeColor"
linktitle: "get_ForeThemeColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_ForeThemeColor. يحصل على أو يضبط كائن ThemeColor الذي يمثل لون المقدمة للخط في C++."
type: docs
weight: 10334
url: /ar/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


يحصل أو يضبط كائن ThemeColor الذي يمثل لون مقدمة الخط.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## أمثلة



يوضح كيفية ضبط لون السمة الأمامية وتدرج اللون والظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## انظر أيضًا

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
