---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Clear method"
linktitle: "Clear"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Clear method. Bu koleksiyondaki tüm ChartSeries'i C++'ta kaldırır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection::Clear method


Bu koleksiyondaki tüm [ChartSeries](../../chartseries/) kaldırır.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesCollection::Clear()
```


## Örnekler



Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Varsayılan olarak üç demo veri serisi içerecek bir sütun grafiği ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Her seri dört ondalık değere sahiptir: dört kategoriden her biri için bir değer.
// Bu veriyi dört küme üç sütun temsil edecek.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Grafikteki her serinin adını yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Bunlar grafikteki kategorilerin adlarıdır.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Mevcut kategoriler için yeni değerlerle bir seri ekleyebiliriz.
// Bu grafik artık dört sütundan oluşan dört küme içerecek.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Bir grafik serisi indeksle de kaldırılabilir, şöyle.
// Bu, grafikle gelen üç demo serisinden birini kaldıracak.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Bu yöntemle grafiğin tüm verilerini bir anda temizleyebiliriz.
// Yeni bir grafik oluştururken, tüm demo verileri silmenin yolu budur
// boş bir grafik üzerinde çalışmaya başlamadan önce.
chartData->Clear();
```

## Ayrıca Bakınız

* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
