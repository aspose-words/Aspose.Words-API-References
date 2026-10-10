---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator metod"
linktitle: "get_Separator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator metod. Hämtar eller anger teckenseparatorn som används för dataetiketterna för hela serien. Standardvärdet är ett kommatecken, förutom för pajdiagram som bara visar kategorinamn och procent, då ett radbryt ska användas istället i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


Hämtar eller anger strängseparatorn som används för dataetiketterna i hela serien. Standardvärdet är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procentandel, då en radbrytning ska användas istället.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
```


## Exempel



Visar hur man arbetar med dataetiketter i ett bubbeldiagram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Lägg till en anpassad serie med X/Y-koordinater och diametern för varje bubbla.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Aktivera dataetiketter och ändra sedan deras utseende.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```


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
