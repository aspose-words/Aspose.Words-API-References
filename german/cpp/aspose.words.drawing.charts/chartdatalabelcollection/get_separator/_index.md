---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator Methode"
linktitle: "get_Separator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator Methode. Ruft das Zeichen für die Trennung von Zeichenketten ab oder legt es fest, das für die Datenbeschriftungen der gesamten Serie verwendet wird. Standardmäßig ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und Prozentsatz anzeigen, wo stattdessen ein Zeilenumbruch verwendet werden soll in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


Liest oder legt das Zeichen zur Trennung von Zeichenketten für die Datenbeschriftungen der gesamten Serie fest. Standardmäßig ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und Prozentsatz anzeigen, dann wird stattdessen ein Zeilenumbruch verwendet.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
```


## Beispiele



Zeigt, wie man mit Datenbeschriftungen eines Blasendiagramms arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine benutzerdefinierte Serie mit X/Y-Koordinaten und dem Durchmesser jeder Blase hinzu.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Aktivieren Sie Datenbeschriftungen und ändern Sie anschließend deren Aussehen.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```


Zeigt, wie man mit Datenbeschriftungen eines Kreisdiagramms arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine benutzerdefinierte Diagrammreihe mit einem Kategorienamen für jeden Sektor und deren Häufigkeitstabelle ein.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Aktivieren Sie Datenbeschriftungen, die sowohl Prozentsatz als auch Häufigkeit jedes Sektors anzeigen, und ändern Sie deren Aussehen.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Siehe auch

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
