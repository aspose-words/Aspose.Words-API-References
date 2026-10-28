---
title: Aspose::Words::Drawing::Stroke::set_BackTintAndShade method
linktitle: set_BackTintAndShade
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::set_BackTintAndShade method. Sets a double value that lightens or darkens the stroke background color in C++.'
type: docs
weight: 24667
url: /cpp/aspose.words.drawing/stroke/set_backtintandshade/
---
## Stroke::set_BackTintAndShade method


Sets a double value that lightens or darkens the stroke background color.

```cpp
void Aspose::Words::Drawing::Stroke::set_BackTintAndShade(double value)
```

## Remarks


 The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in **ArgumentOutOfRangeException**.
## Examples


Shows how to set back theme color and tint and shade.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Stroke gradient outline.docx"));

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```
## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
