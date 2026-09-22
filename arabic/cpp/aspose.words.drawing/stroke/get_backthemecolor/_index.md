---
title: "طريقة Aspose::Words::Drawing::Stroke::get_BackThemeColor"
linktitle: "get_BackThemeColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Stroke::get_BackThemeColor. يحصل على أو يضبط كائن ThemeColor الذي يمثل لون خلفية الخط في C++."
type: docs
weight: 2167
url: /ar/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


يحصل أو يعيّن كائن ThemeColor الذي يمثل لون خلفية الحد.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## أمثلة



يوضح كيفية تعيين لون السمة الخلفية وتدرّج اللون والظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## انظر أيضًا

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
