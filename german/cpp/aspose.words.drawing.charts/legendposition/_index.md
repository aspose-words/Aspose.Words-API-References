---
title: "Aspose::Words::Drawing::Charts::LegendPosition Aufzählung"
linktitle: "LegendPosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::LegendPosition Aufzählung. Gibt die möglichen Positionen einer Diagrammlegende in C++ an."
type: docs
weight: 29000
url: /de/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Gibt die möglichen Positionen für eine Diagrammlegende an.

```cpp
enum class LegendPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Für das Diagramm wird keine Legende angezeigt. |
| Unten | 1 | Gibt an, dass die Legende am unteren Rand des Diagramms gezeichnet wird. |
| Links | 2 | Gibt an, dass die Legende am linken Rand des Diagramms gezeichnet wird. |
| Rechts | 3 | Gibt an, dass die Legende am rechten Rand des Diagramms gezeichnet wird. |
| Oben | 4 | Gibt an, dass die Legende am oberen Rand des Diagramms gezeichnet wird. |
| TopRight | 5 | Gibt an, dass die Legende oben rechts im Diagramm gezeichnet wird. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
