---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. Eksen başlığı özelliklerine erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 5750
url: /tr/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Eksen başlığı özelliklerine erişim sağlar. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartAxisTitle : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Font](./get_font/)() | Eksen başlığının yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Format](./get_format/)() | Eksen başlığının dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_Orientation](./get_orientation/)() | Eksen başlığı metninin yönünü alır veya ayarlar. |
| [get_Overlay](./get_overlay/)() | Diğer grafik öğelerinin başlığın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan değer **false**dır. |
| [get_Rotation](./get_rotation/)() | Eksen başlığının dönüşünü derece cinsinden alır veya ayarlar. |
| [get_Show](./get_show/)() | Başlığın eksen için gösterilip gösterilmeyeceğini belirler. Varsayılan değer **false**dır. |
| [get_Text](./get_text/)() | Eksen başlığının metnini alır veya ayarlar. **null** veya boş değer belirtilirse, otomatik oluşturulan başlık gösterilir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/) için ayarlayıcı. |
| [set_Overlay](./set_overlay/)(bool) | [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/) için ayarlayıcı. |
| [set_Rotation](./set_rotation/)(int32_t) | [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/) için ayarlayıcı. |
| [set_Show](./set_show/)(bool) | [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/) için ayarlayıcı. |
| [set_Text](./set_text/)(const System::String\&) | [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Grafik eksen başlığının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Varsayılan oluşturulan seriyi sil.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
