---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metod"
linktitle: "get_FormatCode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metod. Hämtar eller anger formatkoden som tillämpas på en datamärkning i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Hämtar eller anger formatkoden som tillämpas på en datamärkning.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Anmärkningar


Nummerformatering används för att ändra hur ett värde visas i en datamärkning och kan användas på mycket kreativa sätt. Exempel på nummerformat:

Tal - "#,##0.00"

Valuta - "\"\$\\"#,##0.00"

Tid - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Procent - "0.00%"

Bråk - "# ?/?"

Vetenskaplig - "0.00E+00"

Text - "@"

Bokföring - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Anpassad med färg - "[Red]-#,##0.0"

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


Visar hur man anger formatering för diagramvärden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Lägg till en anpassad serie i diagrammet med kategorier för X-axeln,
// och stora respektive numeriska värden för Y-axeln.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Ställ in talformatet för Y-axelns tick-etiketter så att siffror inte grupperas med kommatecken.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Denna flagga kan åsidosätta värdet ovan och hämta talformatet från källcellen.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Se även

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
