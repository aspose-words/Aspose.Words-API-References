---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get metodu. Belirtilen indeksteki bir ChartSeriesGroup döndürür C++'da."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/idx_get/
---
## ChartSeriesGroupCollection::idx_get method


Belirtilen indeksteki bir [ChartSeriesGroup](../../chartseriesgroup/) döndürür.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get(int32_t index)
```


## Örnekler



İkincil ekseni nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// İkincil ekseni bulun ve koleksiyondan kaldırın.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## Ayrıca Bakınız

* Class [ChartSeriesGroup](../../chartseriesgroup/)
* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
