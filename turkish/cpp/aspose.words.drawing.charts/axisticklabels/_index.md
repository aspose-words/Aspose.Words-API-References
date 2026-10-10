---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels sınıfı"
linktitle: "AxisTickLabels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels sınıfı. C++'ta eksen işaretleme etiketi özelliklerini temsil eder."
type: docs
weight: 3250
url: /tr/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


Eksen işaret işareti etiketlerinin özelliklerini temsil eder.

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Eksen işaretleme etiketlerinin metin hizalamasını alır veya ayarlar. |
| [get_Font](./get_font/)() | İşaretleme etiketlerinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_IsAutoSpacing](./get_isautospacing/)() | İşaretleme etiketlerini çizerken otomatik aralık kullanılacağını gösteren bir bayrağı alır veya ayarlar. |
| [get_Offset](./get_offset/)() | İşaretleme etiketlerinin eksenden uzaklığını alır veya ayarlar. |
| [get_Orientation](./get_orientation/)() | İşaretleme etiketi metninin yönünü alır veya ayarlar. |
| [get_Position](./get_position/)() | İşaretleme etiketlerinin eksen üzerindeki konumunu alır veya ayarlar. |
| [get_Rotation](./get_rotation/)() | İşaretleme etiketlerinin derece cinsinden dönüşünü alır veya ayarlar. |
| [get_Spacing](./get_spacing/)() | Tik etiketlerinin çizildiği aralığı alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/). |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/). |
| [set_Offset](./set_offset/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/). |
| [set_Spacing](./set_spacing/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/). |
| static [Type](./type/)() |  |

## Örnekler



Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// X ekseni için kategoriler ve Y ekseni için ilgili sayısal değerlerle bir grafik serisi ekleyin.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Grafik eksenlerinin görünümünü değiştirebilecek çeşitli seçenekleri vardır,
// örneğin yönleri, ana/alt birim işaretçileri ve işaretlemeler.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Sütun grafiklerinde Z ekseni bulunmaz.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
