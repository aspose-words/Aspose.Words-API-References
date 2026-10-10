---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName Methode"
linktitle: "get_ShowCategoryName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName Methode. Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showcategoryname/
---
## ChartDataLabelCollection::get_ShowCategoryName method


Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Standardwert ist **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName()
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

## Siehe auch

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
