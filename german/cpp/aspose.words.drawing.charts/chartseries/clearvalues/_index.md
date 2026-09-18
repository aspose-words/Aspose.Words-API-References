---
title: "Aspose::Words::Drawing::Charts::ChartSeries::ClearValues Methode"
linktitle: "ClearValues"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::ClearValues Methode. Entfernt alle Datenwerte aus der Diagrammserie und bewahrt dabei das Format der Datenpunkte und Datenbeschriftungen in C++."
type: docs
weight: 1750
url: /de/cpp/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries::ClearValues method


Entfernt alle Datenwerte aus der Diagrammserie, wobei das Format der Datenpunkte und Datenbeschriftungen erhalten bleibt.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::ClearValues()
```


## Beispiele



Zeigt, wie Diagrammreihen mit Daten gefüllt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Löscht X‑ und Y‑Werte der ersten Reihe.
series1->ClearValues();

// Füllen Sie die Reihe mit Daten.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Löscht X‑ und Y‑Werte der zweiten Reihe.
series2->Clear();

// Füllen Sie die Reihe mit Daten.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Siehe auch

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
