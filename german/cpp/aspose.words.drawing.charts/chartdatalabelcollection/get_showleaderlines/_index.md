---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines Methode"
linktitle: "get_ShowLeaderLines"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines Methode. Ermöglicht die Angabe, ob Leitlinien der Datenbeschriftungen für die gesamte Serie angezeigt werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showleaderlines/
---
## ChartDataLabelCollection::get_ShowLeaderLines method


Ermöglicht die Angabe, ob Führungslinien der Datenbeschriftungen für die Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines()
```

## Hinweise


Gilt nur für Kreisdiagramme. Leitlinien erzeugen eine visuelle Verbindung zwischen einer Datenbeschriftung und dem zugehörigen Datenpunkt.

Der für diese Eigenschaft definierte Wert kann für eine einzelne Datenbeschriftung überschrieben werden, indem die [ShowLeaderLines](../../chartdatalabel/get_showleaderlines/) Eigenschaft verwendet wird.

## Beispiele



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
