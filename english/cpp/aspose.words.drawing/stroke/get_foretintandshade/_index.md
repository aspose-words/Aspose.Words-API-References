---
title: Aspose::Words::Drawing::Stroke::get_ForeTintAndShade method
linktitle: get_ForeTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::get_ForeTintAndShade method. Gets or sets a double value that lightens or darkens the stroke foreground color in C++.'
type: docs
weight: 10667
url: /cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Gets or sets a double value that lightens or darkens the stroke foreground color.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Remarks


The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in [ArgumentOutOfRangeException](../).

## Examples



Shows how to set fore theme color and tint and shade. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
