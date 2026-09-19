---
title: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metodo"
linktitle: "get_ForeThemeColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Fill::get_ForeThemeColor metodo. Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano per il riempimento in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano per il riempimento.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## Esempi



Mostra come impostare il colore del tema per il colore della forma in primo piano/sfondo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Nota: non utilizzare "BackThemeColor" e "BackTintAndShade" per il riempimento del carattere.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Vedi anche

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
