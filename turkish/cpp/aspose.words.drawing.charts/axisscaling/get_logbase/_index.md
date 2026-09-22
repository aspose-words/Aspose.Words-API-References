---
title: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase metodu"
linktitle: "get_LogBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase metodu. C++'de logaritmik bir eksen için logaritmik tabanı alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


Logaritmik eksen için logaritmik tabanı alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## Açıklamalar


Bu özellik, MS Office 2016 yeni grafikler tarafından desteklenmez.

Kayan nokta değerinin geçerli aralığı 2'ye eşit veya büyük ve 1000'e eşit veya küçüktür. Özellik yalnızca [Type](../get_type/) [Logarithmic](../../axisscaletype/) olarak ayarlandığında etkili olur.

Bu özelliği ayarlamak, [Type](../get_type/) özelliğini [Logarithmic](../../axisscaletype/) olarak ayarlar.

## Örnekler



Bir grafik eksenine logaritmik ölçekleme nasıl uygulanır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// Beş nokta için X/Y koordinatları içeren bir seri ekleyin.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// X ekseninin ölçeklemesi varsayılan olarak doğrusaldır,
// eşit artan değerleri göstererek X-değer aralığımızı (0, 1, 2, 3...) kapsar.
// Doğrusal bir eksen Y değerlerimiz için ideal değildir
// çünkü daha küçük Y değerlerine sahip noktalar okunması daha zor olacaktır.
// 20 tabanlı bir logaritmik ölçekleme (1, 20, 400, 8000...)
// çizilen noktaları yayar, böylece grafik üzerindeki değerlerini daha kolay okuyabiliriz.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Ayrıca Bakınız

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
