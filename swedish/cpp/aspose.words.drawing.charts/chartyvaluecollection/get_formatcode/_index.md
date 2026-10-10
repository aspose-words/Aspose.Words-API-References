---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode method"
linktitle: "get_FormatCode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode method. Hämtar eller anger formatkoden som tillämpas på Y‑värdena i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.drawing.charts/chartyvaluecollection/get_formatcode/
---
## ChartYValueCollection::get_FormatCode method


Hämtar eller anger formatkoden som tillämpas på Y‑värdena.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode()
```

## Anmärkningar


Talformatering används för att ändra hur värden visas i diagrammet. Exempel på talformat:

Tal - "#,##0.00"

Valuta - "\"\$\\"#,##0.00"

Tid - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Procent - "0.00%"

Bråk - "# ?/?"

Vetenskaplig - "0.00E+00"

Bokföring - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Anpassad med färg - "[Red]-#,##0.0"

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

* Class [ChartYValueCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
