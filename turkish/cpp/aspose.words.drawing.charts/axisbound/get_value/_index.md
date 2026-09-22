---
title: "Aspose::Words::Drawing::Charts::AxisBound::get_Value metodu"
linktitle: "get_Value"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisBound::get_Value metodu. C++'ta eksen sınırlamasının sayısal değerini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing.charts/axisbound/get_value/
---
## AxisBound::get_Value method


Eksen sınırının sayısal değerini döndürür.

```cpp
double Aspose::Words::Drawing::Charts::AxisBound::get_Value() const
```


## Örnekler



Özel eksen sınırlarının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// İki ondalık dizi içeren bir seri ekleyin. İlk dizi X değerlerini içerir,
// ve ikincisi dağılım grafiğindeki noktalar için karşılık gelen Y değerlerini içerir.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// Varsayılan olarak, grafiğin X ve Y eksenlerine varsayılan ölçekleme uygulanır,
// böylece her iki eksenin aralıkları, her serinin tüm X ve Y değerlerini kapsayacak kadar geniş olur.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// Kendi eksen sınırlarımızı tanımlayabiliriz.
// Bu durumda, hem X hem de Y ekseni ölçerlerini 0 ile 10 arasında bir aralık gösterecek şekilde ayarlayacağız.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// X ekseninde tarih aralığı gerektiren ve Y ekseninde ondalık değerler içeren bir seri ile bir çizgi grafiği oluşturun.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// Ayrıca eksen sınırlarını tarih biçiminde ayarlayabilir, grafiği belirli bir döneme sınırlayabiliriz.
// Aralığı 1980-1990 olarak ayarlamak, serinin iki değerini dışarı bırakacaktır
// grafiğin aralığının dışında olanları.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## Ayrıca Bakınız

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
