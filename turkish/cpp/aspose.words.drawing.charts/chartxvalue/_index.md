---
title: "Aspose::Words::Drawing::Charts::ChartXValue sınıfı"
linktitle: "ChartXValue"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartXValue sınıfı. C++'ta bir grafik serisi için X değerini temsil eder."
type: docs
weight: 18200
url: /tr/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Bir grafik serisi için X değerini temsil eder.

```cpp
class ChartXValue : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut X değeri nesnesine eşit olup olmadığını gösteren bir bayrak alır. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Bir [ChartXValue](./) örneği, [DateTime](../chartxvaluetype/) türünden oluşturur. |
| static [FromDouble](./fromdouble/)(double) | Bir [ChartXValue](./) örneği, [Double](../chartxvaluetype/) türünden oluşturur. |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Bir [ChartXValue](./) örneği, [Multilevel](../chartxvaluetype/) türünden oluşturur. |
| static [FromString](./fromstring/)(const System::String\&) | Bir [ChartXValue](./) örneği, [String](../chartxvaluetype/) türünden oluşturur. |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Bir [ChartXValue](./) örneği, [Time](../chartxvaluetype/) türünden oluşturur. |
| [get_DateTimeValue](./get_datetimevalue/)() const | Depolanan tarih‑zaman değerini alır. |
| [get_DoubleValue](./get_doublevalue/)() const | Depolanan sayısal değeri alır. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Depolanan çok seviyeli değeri alır. |
| [get_StringValue](./get_stringvalue/)() const | Depolanan dize değerini alır. |
| [get_TimeValue](./get_timevalue/)() const | Depolanan zaman değerini alır. |
| [get_ValueType](./get_valuetype/)() const | Nesnede depolanan X değerinin tipini alır. |
| [GetHashCode](./gethashcode/)() const override | Mevcut X değer nesnesi için bir karma kodu alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıf, belirli bir tipte X değeri oluşturmak için bir dizi statik yöntem içerir. [ValueType](./get_valuetype/) özelliği, mevcut bir X değerinin tipini belirlemenizi sağlar.

Bir grafik serisinin tüm null olmayan X değerleri aynı [ChartXValueType](../chartxvaluetype/) tipinde olmalıdır.

## Örnekler



Grafik serilerini veriyle doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// İlk serinin X ve Y değerlerini temizle.
series1->ClearValues();

// Seriyi veriyle doldur.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// İkinci serinin X ve Y değerlerini temizle.
series2->Clear();

// Seriyi veriyle doldur.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
