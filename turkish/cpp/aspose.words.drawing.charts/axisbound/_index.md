---
title: "Aspose::Words::Drawing::Charts::AxisBound sınıf"
linktitle: "AxisBound"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisBound sınıf. Eksen değerlerinin minimum veya maksimum sınırını temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Eksen değerlerinin minimum veya maksimum sınırını temsil eder. Daha fazla bilgi edinmek için [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class AxisBound : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [AxisBound](./axisbound/)() | Bir kelime işlem uygulaması tarafından eksen sınırının otomatik olarak belirlenmesi gerektiğini gösteren yeni bir örnek oluşturur. |
| [AxisBound](./axisbound/)(double) | Sayısal olarak temsil edilen bir eksen sınırı oluşturur. |
| [AxisBound](./axisbound/)(System::DateTime) | Tarih saat değeri olarak temsil edilen bir eksen sınırı oluşturur. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_IsAuto](./get_isauto/)() const | Eksen sınırının otomatik olarak belirlenmesi gerektiğini gösteren bir bayrak döndürür. |
| [get_Value](./get_value/)() const | Eksen sınırının sayısal değerini döndürür. |
| [get_ValueAsDate](./get_valueasdate/)() | Eksen sınırının tarih saat olarak temsil edilen değerini döndürür. |
| [GetHashCode](./gethashcode/)() const override | Bu tip için bir karma (hash) işlevi olarak hizmet verir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür. |
| static [Type](./type/)() |  |
## Açıklamalar


Sınır, sayısal, tarih saat veya özel "auto" değeri olarak belirtilebilir.

Bu sınıfın örnekleri değiştirilemez.

## Örnekler



Tarih/saat değerleriyle grafik eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// X ekseni için tarih/saat değerleri ve Y ekseni için ilgili ondalık değerler içeren özel bir seri ekleyin.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// X ekseni için alt ve üst sınırları ayarlayın.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// X ekseninin ana birimlerini bir hafta, alt birimlerini bir gün olarak ayarlayın.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Ondalık değerler için Y ekseni özelliklerini tanımlayın.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
