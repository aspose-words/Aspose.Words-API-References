---
title: Aspose::Words::Drawing::Stroke::get_BackThemeColor method
linktitle: get_BackThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::get_BackThemeColor method. Gets or sets a ThemeColor object that represents the stroke background color in C++.'
type: docs
weight: 2167
url: /cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


Gets or sets a ThemeColor object that represents the stroke background color.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## Examples



Shows how to set back theme color and tint and shade. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## See Also

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
