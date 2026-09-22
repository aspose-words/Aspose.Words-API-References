---
title: "Aspose::Words::Drawing::Charts::ChartAxisCollection sınıfı"
linktitle: "ChartAxisCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxisCollection sınıfı. C++'da bir grafik eksenleri koleksiyonunu temsil eder."
type: docs
weight: 5500
url: /tr/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


Grafik eksenlerinin bir koleksiyonunu temsil eder.

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Bu koleksiyondaki eksen sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki ekseni alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
