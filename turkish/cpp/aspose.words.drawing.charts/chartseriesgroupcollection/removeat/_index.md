---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt yöntemi"
linktitle: "RemoveAt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt yöntemi. Belirtilen indeksteki bir seri grubunu kaldırır. Tüm alt seriler C++'ta grafikten kaldırılacaktır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection::RemoveAt method


Belirtilen indeksteki bir seri grubunu kaldırır. Tüm alt seriler grafikten kaldırılacaktır.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt(int32_t index)
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

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
