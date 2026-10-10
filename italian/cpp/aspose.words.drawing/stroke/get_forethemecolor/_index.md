---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metodo"
linktitle: "get_ForeThemeColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor metodo. Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano del tratto in C++."
type: docs
weight: 10334
url: /it/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano del tratto.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Esempi



Mostra come impostare il colore del tema di primo piano e la tinta e l'ombreggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Vedi anche

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
