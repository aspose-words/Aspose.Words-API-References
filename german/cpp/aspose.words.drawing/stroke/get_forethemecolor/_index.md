---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor Methode"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor Methode. Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Vordergrundfarbe des Strichs in C++ darstellt."
type: docs
weight: 10334
url: /de/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Liest oder setzt ein ThemeColor-Objekt, das die Vordergrundfarbe des Strichs darstellt.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Beispiele



Zeigt, wie man die Vordergrund‑Designfarbe sowie Farbton und Schattierung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Siehe auch

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
