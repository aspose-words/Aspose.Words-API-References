---
title: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups yöntemi"
linktitle: "get_SeriesGroups"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups yöntemi. C++'ta bu grafiğin bir seri grubu koleksiyonuna erişim sağlar."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


Bu çizelgenin seri grup koleksiyonuna erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


## Örnekler



Boşluk genişliği ve örtüşmeyi nasıl yapılandıracağınızı gösterin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Sütun boşluk genişliğini ve örtüşmeyi ayarlayın.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Ayrıca Bakınız

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
