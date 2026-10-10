---
title: "Aspose::Words::Drawing::Charts::ChartYValue class"
linktitle: "ChartYValue"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartYValue sınıfı. C++'da bir grafik serisi için Y değerini temsil eder."
type: docs
weight: 18600
url: /tr/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Bir grafik serisi için Y değerini temsil eder.

```cpp
class ChartYValue : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut Y değeri nesnesine eşit olup olmadığını gösteren bir bayrak alır. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | [ChartYValue](./) tipinde bir [DateTime](../chartyvaluetype/) örneği oluşturur. |
| static [FromDouble](./fromdouble/)(double) | [ChartYValue](./) tipinde bir [Double](../chartyvaluetype/) örneği oluşturur. |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | [ChartYValue](./) tipinde bir [Time](../chartyvaluetype/) örneği oluşturur. |
| [get_DateTimeValue](./get_datetimevalue/)() const | Depolanan tarih‑zaman değerini alır. |
| [get_DoubleValue](./get_doublevalue/)() const | Depolanan sayısal değeri alır. |
| [get_TimeValue](./get_timevalue/)() const | Depolanan zaman değerini alır. |
| [get_ValueType](./get_valuetype/)() const | Nesnede depolanan Y değerinin tipini alır. |
| [GetHashCode](./gethashcode/)() const override | Mevcut Y değeri nesnesi için bir hash kodu alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıf, belirli bir tipte Y değeri oluşturmak için bir dizi statik yöntem içerir. [ValueType](./get_valuetype/) özelliği, mevcut bir Y değerinin tipini belirlemenizi sağlar.

Bir grafik serisinin tüm null olmayan Y değerleri aynı [ChartYValueType](../chartyvaluetype/) tipinde olmalıdır.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
