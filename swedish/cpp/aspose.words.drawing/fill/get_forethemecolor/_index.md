---
title: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metod"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metod. Hämtar eller anger ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


Hämtar eller anger ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## Exempel



Visar hur man ställer in temafärg för förgrunds-/bakgrundsfärg på en figur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Obs: använd inte "BackThemeColor" och "BackTintAndShade" för teckenfyllning.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Se även

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
