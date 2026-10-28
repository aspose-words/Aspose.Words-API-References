---
title: Aspose::Words::Drawing::Stroke::set_ForeThemeColor method
linktitle: set_ForeThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::set_ForeThemeColor method. Sets a ThemeColor object that represents the stroke foreground color in C++.'
type: docs
weight: 32334
url: /cpp/aspose.words.drawing/stroke/set_forethemecolor/
---
## Stroke::set_ForeThemeColor method


Sets a ThemeColor object that represents the stroke foreground color.

```cpp
void Aspose::Words::Drawing::Stroke::set_ForeThemeColor(Aspose::Words::Themes::ThemeColor value)
```

## Examples


Shows how to set fore theme color and tint and shade.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::TextBox, static_cast<double>(100), static_cast<double>(40));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```
## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
