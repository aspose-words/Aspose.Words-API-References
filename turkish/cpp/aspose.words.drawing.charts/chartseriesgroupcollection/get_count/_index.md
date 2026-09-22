---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count yöntemi"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count yöntemi. Bu koleksiyondaki seri grup sayısını C++'ta döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/get_count/
---
## ChartSeriesGroupCollection::get_Count method


Bu koleksiyondaki seri gruplarının sayısını döndürür.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count()
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
