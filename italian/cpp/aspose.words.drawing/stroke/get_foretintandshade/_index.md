---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metodo"
linktitle: "get_ForeTintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano del tratto in C++."
type: docs
weight: 10667
url: /it/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano del tratto.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Note


I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Tentare di impostare questa proprietà a un valore inferiore a -1 o superiore a 1 genera un [ArgumentOutOfRangeException](../).

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

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
