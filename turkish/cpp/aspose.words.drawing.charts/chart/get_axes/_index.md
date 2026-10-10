---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes metodu"
linktitle: "get_Axes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes metodu. C++'ta bu grafiğin tüm eksenlerinin bir koleksiyonunu alır."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## Örnekler



Eksen koleksiyonuyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Birincil ve ikincil Y eksenlerindeki ana ızgara çizgilerini gizle.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Ayrıca Bakınız

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
