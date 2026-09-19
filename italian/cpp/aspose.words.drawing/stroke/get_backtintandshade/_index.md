---
title: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade metodo"
linktitle: "get_BackTintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo del tratto in C++."
type: docs
weight: 2334
url: /it/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo del tratto.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Note


I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Tentare di impostare questa proprietà a un valore inferiore a -1 o superiore a 1 genera un [ArgumentOutOfRangeException](../).

## Esempi



Mostra come impostare il colore del tema di sfondo e la tinta e l'ombreggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Vedi anche

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
