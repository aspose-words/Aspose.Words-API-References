---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels metod"
linktitle: "get_HasDataLabels"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels metod. Hämtar eller anger en flagga som visar om dataetiketter visas för serien i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing.charts/chartseries/get_hasdatalabels/
---
## ChartSeries::get_HasDataLabels method


Hämtar eller anger en flagga som indikerar om datamärkningar visas för serien.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels() const
```


## Exempel



Visar hur man aktiverar och konfigurerar dataetiketter för en diagramserie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till ett linjediagram, rensa sedan dess demodata-serier för att börja med ett rent diagram,
// och sätt sedan en titel.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Infoga en anpassad diagramserie med månader som kategorier för X‑axeln,
// och respektive decimala belopp för Y‑axeln.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Aktivera dataetiketter och tillämpa sedan ett anpassat talformat för värden som visas i dataetiketterna.
// Detta format kommer att behandla visade decimala värden som miljoner amerikanska dollar.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## Se även

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
