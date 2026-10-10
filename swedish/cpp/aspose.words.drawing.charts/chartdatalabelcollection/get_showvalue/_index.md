---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue metod"
linktitle: "get_ShowValue"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue metod. Tillåter att ange om värden ska visas i datamärkningarna för hela serien. Standardvärdet är falskt i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showvalue/
---
## ChartDataLabelCollection::get_ShowValue method


Tillåter att ange om värden ska visas i dataetiketterna i hela serien. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue()
```


## Exempel



Visar hur man arbetar med dataetiketter i ett pajdiagram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Infoga en anpassad diagramserie med ett kategorinamn för varje sektor och deras frekvenstabell.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Aktivera dataetiketter som visar både procent och frekvens för varje sektor och ändra deras utseende.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Se även

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
