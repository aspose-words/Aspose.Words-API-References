---
title: Aspose::Words::Drawing::Fill::set_BackTintAndShade method
linktitle: set_BackTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::set_BackTintAndShade method. Sets a double value that lightens or darkens the background color in C++.'
type: docs
weight: 69000
url: /cpp/aspose.words.drawing/fill/set_backtintandshade/
---
## Fill::set_BackTintAndShade method


Sets a double value that lightens or darkens the background color.

```cpp
void Aspose::Words::Drawing::Fill::set_BackTintAndShade(double value)
```

## Remarks


The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.
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
## Exceptions

* **ArgumentOutOfRangeException** - Throw if set this property to a value less than -1 or more than 1.

## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
