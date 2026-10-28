---
title: Aspose::Words::Drawing::Fill::set_ForeThemeColor method
linktitle: set_ForeThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::set_ForeThemeColor method. Sets a ThemeColor object that represents the foreground color for the fill in C++.'
type: docs
weight: 72000
url: /cpp/aspose.words.drawing/fill/set_forethemecolor/
---
## Fill::set_ForeThemeColor method


Sets a ThemeColor object that represents the foreground color for the fill.

```cpp
void Aspose::Words::Drawing::Fill::set_ForeThemeColor(Aspose::Words::Themes::ThemeColor value)
```

## Examples


Shows how to set theme color for foreground/background shape color.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::RoundRectangle, static_cast<double>(80), static_cast<double>(80));

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(ThemeColor::Dark1);
fill->set_BackThemeColor(ThemeColor::Background2);

// Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```
## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
