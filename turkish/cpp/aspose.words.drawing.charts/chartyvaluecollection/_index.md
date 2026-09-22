---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection sınıfı"
linktitle: "ChartYValueCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection sınıfı. C++'ta bir grafik serisi için Y değerlerinin bir koleksiyonunu temsil eder."
type: docs
weight: 18800
url: /tr/cpp/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class


Bir grafik serisi için Y değerlerinin bir koleksiyonunu temsil eder.

```cpp
class ChartYValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Bu koleksiyondaki öğe sayısını alır. |
| [get_FormatCode](./get_formatcode/)() | Y değerlerine uygulanan biçim kodunu alır veya ayarlar. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki Y değerini alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Belirtilen indeksteki Y değerini alır veya ayarlar. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Açıklamalar


Koleksiyonun **null** dışındaki tüm öğeleri aynı [ValueType](../chartyvalue/get_valuetype/) değerine sahip olmalıdır.

Koleksiyon yalnızca Y değerlerini değiştirmeye izin verir. Bir grafik serisine yeni değerler eklemek veya eklemek, ya da değerleri kaldırmak için, [ChartSeries](../chartseries/) sınıfının uygun yöntemleri kullanılabilir.

## Örnekler



Grafik serisi verilerinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // Tüm veri noktalarının bireysel biçimini temizle.
    // Sütun grafiklerde veri noktaları ve veri değerleri bire bir eşleşir.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Y değerini al.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Maksimum ve minimum değerlerin renklerini değiştir.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
