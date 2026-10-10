---
title: "Metodo Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation"
linktitle: "get_Orientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation. Ottiene o imposta l'orientamento del testo delle etichette dei segni in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Ottiene o imposta l'orientamento del testo delle etichette dei segni di graduazione.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Note


Il valore predefinito è [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Nota che alcuni valori di [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) non influenzano l'orientamento del testo delle etichette dei segni negli assi dei valori.

## Esempi



Mostra come modificare l'orientamento e la rotazione delle etichette di graduazione dell'asse.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a colonne.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Imposta l'orientamento e la rotazione delle etichette di graduazione dell'asse.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Vedi anche

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
