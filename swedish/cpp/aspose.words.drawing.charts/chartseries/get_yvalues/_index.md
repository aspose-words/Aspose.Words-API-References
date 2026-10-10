---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues metod"
linktitle: "get_YValues"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues metod. Hämtar en samling av Y‑värden för denna diagramserie i C++."
type: docs
weight: 12667
url: /sv/cpp/aspose.words.drawing.charts/chartseries/get_yvalues/
---
## ChartSeries::get_YValues method


Hämtar en samling av Y‑värden för denna diagramserie.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValueCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_YValues()
```


## Exempel



Visar hur man arbetar med formatkoden för diagramdata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett bubbeldiagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Ta bort standardgenererad serie.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Visa datamärkningar.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Ställ in dataformatkoder.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Se även

* Class [ChartYValueCollection](../../chartyvaluecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
