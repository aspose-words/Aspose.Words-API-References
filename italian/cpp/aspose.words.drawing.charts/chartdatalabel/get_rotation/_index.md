---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation metodo"
linktitle: "get_Rotation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation metodo. Ottiene o imposta la rotazione dell'etichetta in gradi in C++."
type: docs
weight: 7667
url: /it/cpp/aspose.words.drawing.charts/chartdatalabel/get_rotation/
---
## ChartDataLabel::get_Rotation method


Ottiene o imposta la rotazione dell'etichetta in gradi.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation()
```

## Note


L'intervallo di valori accettabili è da -180 a 180 inclusi. Il valore predefinito è 0.

Se il valore [Orientation](../get_orientation/) è [Horizontal](../../../aspose.words.drawing/shapetextorientation/), la forma dell'etichetta, se esiste, viene ruotata insieme al testo dell'etichetta. Altrimenti, solo il testo dell'etichetta viene ruotato.

## Esempi



Mostra come modificare l'orientamento e la rotazione per le etichette dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Mostra le etichette dati.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Definisci la forma dell'etichetta dati.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Imposta l'orientamento e la rotazione dell'etichetta dati per l'intera serie.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Modifica l'orientamento e la rotazione della prima etichetta dati.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Vedi anche

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
