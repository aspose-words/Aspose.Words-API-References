---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove‑metoden"
linktitle: "Ta bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove‑metoden. Tar bort X‑värdet, Y‑värdet och bubbla‑storleken, om det stöds, från diagramserien på det angivna indexet. Den motsvarande datapunkten och datamärket tas också bort i C++."
type: docs
weight: 14500
url: /sv/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Tar bort X‑värdet, Y‑värdet och bubbla‑storleken, om de stöds, från diagramserien på det angivna indexet. Motsvarande datapunkt och datalabel tas också bort.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Exempel



Visar hur man lägger till/ta bort diagramdatavärden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Ta bort det första värdet i båda serierna.
department1Series->Remove(0);
department2Series->Remove(0);

// Lägg till nya värden i båda serierna.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Se även

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
