---
title: "Aspose::Words::Drawing::Charts::LegendPosition enum"
linktitle: "LegendPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::LegendPosition enum. Bir grafik başlığının olası konumlarını C++'da belirtir."
type: docs
weight: 29000
url: /tr/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Bir grafik açıklaması için olası konumları belirtir.

```cpp
enum class LegendPosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Grafik için başlık gösterilmeyecek. |
| Alt | 1 | Başlığın grafiğin altında çizileceğini belirtir. |
| Sol | 2 | Başlığın grafiğin solunda çizileceğini belirtir. |
| Sağ | 3 | Başlığın grafiğin sağında çizileceğini belirtir. |
| Üst | 4 | Başlığın grafiğin üstünde çizileceğini belirtir. |
| ÜstSağ | 5 | Başlığın grafiğin sağ üst köşesinde çizileceğini belirtir. |


## Örnekler



Bir grafiğin lejandının görünümünü nasıl düzenleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Grafiğin lejandını sağ üst köşeye taşıyın.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Grafik gibi diğer grafik öğelerine, lejandın üzerine gelmelerine izin vererek daha fazla alan sağlayın.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
