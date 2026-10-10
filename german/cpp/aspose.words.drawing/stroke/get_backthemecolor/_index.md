---
title: "Aspose::Words::Drawing::Stroke::get_BackThemeColor Methode"
linktitle: "get_BackThemeColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Stroke::get_BackThemeColor Methode. Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Hintergrundfarbe des Strichs in C++ darstellt."
type: docs
weight: 2167
url: /de/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Hintergrundfarbe des Strichs darstellt.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## Beispiele



Zeigt, wie man die Hintergrund-Theme-Farbe sowie Tönung und Schattierung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Siehe auch

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
