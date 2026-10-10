---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt method. Entfernt eine Seriengruppe am angegebenen Index. Alle untergeordneten Serien werden in C++ aus dem Diagramm entfernt."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection::RemoveAt method


Entfernt eine Seriengruppe am angegebenen Index. Alle untergeordneten Serien werden aus dem Diagramm entfernt.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt(int32_t index)
```


## Beispiele



Zeigen Sie, wie man die sekundäre Achse entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// Finden Sie die sekundäre Achse und entfernen Sie sie aus der Sammlung.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## Siehe auch

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
