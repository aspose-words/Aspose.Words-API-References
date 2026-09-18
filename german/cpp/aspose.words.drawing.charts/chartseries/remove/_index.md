---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove Methode"
linktitle: "Remove"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove Methode. Entfernt den X-Wert, Y-Wert und die Blasengröße, falls unterstützt, aus der Diagrammserie am angegebenen Index. Der entsprechende Datenpunkt und die Datenbeschriftung werden ebenfalls in C++ entfernt."
type: docs
weight: 14500
url: /de/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Entfernt den X‑Wert, Y‑Wert und, falls unterstützt, die Blasengröße aus der Diagrammserie an der angegebenen Position. Der entsprechende Datenpunkt und das Datenbeschriftung werden ebenfalls entfernt.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Beispiele



Zeigt, wie Diagrammdatenwerte hinzugefügt/entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Entfernen Sie den ersten Wert in beiden Serien.
department1Series->Remove(0);
department2Series->Remove(0);

// Fügen Sie neue Werte zu beiden Serien hinzu.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Siehe auch

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
