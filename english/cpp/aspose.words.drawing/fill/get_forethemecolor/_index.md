---
title: Aspose::Words::Drawing::Fill::get_ForeThemeColor method
linktitle: get_ForeThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_ForeThemeColor method. Gets or sets a ThemeColor object that represents the foreground color for the fill in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


Gets or sets a ThemeColor object that represents the foreground color for the fill.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## Examples



Shows how to set theme color for foreground/background shape color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## See Also

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
