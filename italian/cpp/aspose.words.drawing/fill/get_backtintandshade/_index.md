---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade metodo"
linktitle: "get_BackTintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Note


I valori consentiti sono nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà.

Zero (0) è neutro.

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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
