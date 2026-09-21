---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource metod"
linktitle: "get_IsLinkedToSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource metod. Anger om formatkoden är länkad till en källcell. Standard är true i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing.charts/chartnumberformat/get_islinkedtosource/
---
## ChartNumberFormat::get_IsLinkedToSource method


Anger om formatkoden är länkad till en källcell. Standard är true.

```cpp
bool Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource()
```


## Exempel



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
