---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Grafik lejandının özelliklerini temsil eder. Daha fazla bilgi edinmek için C++'taki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Grafik lejand özelliklerini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Font](./get_font/)() | Lejand girişlerinin varsayılan yazı tipi biçimlendirmesine erişim sağlar. Belirli bir lejand girişi için yazı tipi biçimlendirmesini geçersiz kılmak için, the[Font](../chartlegendentry/get_font/) özelliğini kullanın. |
| [get_Format](./get_format/)() | Lejandın dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_LegendEntries](./get_legendentries/)() const | Üst grafik için tüm seriler ve trend çizgileri için lejand girişlerinin bir koleksiyonunu döndürür. |
| [get_Overlay](./get_overlay/)() const | Diğer grafik öğelerinin lejandın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan değer **false**'dır. |
| [get_Position](./get_position/)() | Lejandın bir grafikteki konumunu belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Ayarlayıcı, [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/) için. |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Ayarlayıcı, [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/) için. |
| static [Type](./type/)() |  |

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
