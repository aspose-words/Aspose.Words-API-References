---
title: Aspose::Words::Drawing::Stroke::set_BackThemeColor method
linktitle: set_BackThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::set_BackThemeColor method. Sets a ThemeColor object that represents the stroke background color in C++.'
type: docs
weight: 24334
url: /cpp/aspose.words.drawing/stroke/set_backthemecolor/
---
## Stroke::set_BackThemeColor method


Sets a ThemeColor object that represents the stroke background color.

```cpp
void Aspose::Words::Drawing::Stroke::set_BackThemeColor(Aspose::Words::Themes::ThemeColor value)
```

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
