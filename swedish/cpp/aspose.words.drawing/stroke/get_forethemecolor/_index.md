---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metod"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metod. Hämtar eller anger ett ThemeColor‑objekt som representerar linjens förgrundsfärg i C++."
type: docs
weight: 10334
url: /sv/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Hämtar eller anger ett ThemeColor-objekt som representerar streckets förgrundsfärg.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Exempel



Visar hur man anger förgrundstemat färg samt nyans och skugga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Se även

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
