---
title: "Aspose::Words::Drawing::Fill::get_ForeThemeColor Methode"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_ForeThemeColor Methode. Ruft ein ThemeColor-Objekt ab oder legt es fest, das die Vordergrundfarbe für die Füllung in C++ darstellt."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


Liest oder legt ein ThemeColor-Objekt fest, das die Vordergrundfarbe für die Füllung darstellt.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## Beispiele



Zeigt, wie man die Themenfarbe für Vorder-/Hintergrundformenfarbe festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Hinweis: Verwenden Sie nicht "BackThemeColor" und "BackTintAndShade" für die Schriftfüllung.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Siehe auch

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
