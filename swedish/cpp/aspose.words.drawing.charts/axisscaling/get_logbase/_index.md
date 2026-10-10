---
title: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase metod"
linktitle: "get_LogBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase metod. Hämtar eller anger den logaritmiska basen för en logaritmisk axel i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


Hämtar eller anger den logaritmiska basen för en logaritmisk axel.

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## Anmärkningar


Egenskapen stöds inte av de nya diagrammen i MS Office 2016.

Giltigt intervall för ett flyttal är större än eller lika med 2 och mindre än eller lika med 1000. Egenskapen har effekt endast om [Type](../get_type/) är inställd på [Logarithmic](../../axisscaletype/).

Att ställa in denna egenskap sätter [Type](../get_type/) egenskapen till [Logarithmic](../../axisscaletype/).

## Exempel



Visar hur man tillämpar logaritmisk skalning på en diagramaxel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Infoga en serie med X/Y-koordinater för fem punkter.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// Skalningen av X-axeln är linjär som standard,
// visar jämnt ökande värden som täcker vårt X-värdesintervall (0, 1, 2, 3...).
// En linjär axel är inte idealisk för våra Y‑värden
// eftersom punkterna med de mindre Y‑värdena blir svårare att läsa.
// En logaritmisk skalning med basen 20 (1, 20, 400, 8000...)
// kommer att sprida de plottade punkterna, vilket gör det lättare att läsa deras värden i diagrammet.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Se även

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
