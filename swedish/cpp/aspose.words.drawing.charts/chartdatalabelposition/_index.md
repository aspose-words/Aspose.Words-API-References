---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Anger positionen för en diagramdatamärkning i C++."
type: docs
weight: 27334
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Anger positionen för en diagramdatapunktetikett.

```cpp
enum class ChartDataLabelPosition
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Centrerad | 0 | Anger att en datamärkning ska visas centrerad på en datamarkör. |
| Vänster | 1 | Anger att en datamärkning ska visas till vänster om en datamarkör. |
| Höger | 2 | Anger att en datamärkning ska visas till höger om en datamarkör. |
| Ovanför | 3 | Anger att en datamärkning ska visas ovanför en datamarkör. |
| Nedanför | 4 | Anger att en datamärkning ska visas under en datamarkör. |
| InsideBase | 5 | Anger att en datamärkning ska visas inuti basen på en datamarkör. |
| InsideEnd | 6 | Anger att en datamärkning ska visas inuti slutet på en datamarkör. |
| OutsideEnd | 7 | Anger att en datamärkning ska visas utanför slutet på en datamarkör. |
| BestFit | 8 | Anger att en datamärkning ska visas i den mest lämpliga positionen. |


## Exempel



Visar hur man ställer in positionen för dataetiketten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga stapeldiagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Ta bort standardgenererad serie.
seriesColl->Clear();

// Lägg till serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Visa dataetiketter och ställ in teckensnittsfärg.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Ställ in dataetikettens position.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
