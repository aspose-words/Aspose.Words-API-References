---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay-Methode"
linktitle: "get_Overlay"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay-Methode. Bestimmt, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist false in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


Bestimmt, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


## Beispiele



Zeigt, wie das Aussehen der Legende eines Diagramms bearbeitet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Geben Sie anderen Diagrammelementen, wie dem Diagramm selbst, mehr Platz, indem Sie ihnen erlauben, die Legende zu überlappen.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Siehe auch

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
