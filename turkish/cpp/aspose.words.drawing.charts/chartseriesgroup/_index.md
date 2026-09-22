---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup sınıfı"
linktitle: "ChartSeriesGroup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup sınıfı. C++'ta aynı eksenlere bağlı aynı tipteki grafik serilerinin özelliklerini temsil eder, yani bir grafik serisi grubunun özelliklerini temsil eder."
type: docs
weight: 17334
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Bir grafik serisi grubunun özelliklerini temsil eder; yani aynı eksenlere bağlı aynı tipteki grafik serilerinin özelliklerini.

```cpp
class ChartSeriesGroup : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Bu seri grubunun ait olduğu eksen grubunu alır veya ayarlar. |
| [get_AxisX](./get_axisx/)() | Bu seri grubunun X ekseninin özelliklerine erişim sağlar. |
| [get_AxisY](./get_axisy/)() | Bu seri grubunun Y ekseninin özelliklerine erişim sağlar. |
| [get_BubbleScale](./get_bubblescale/)() | Baloncukların boyutunu varsayılan boyutlarının yüzdesi olarak alır veya ayarlar. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Üst dönen çember grafiğinin delik boyutunu yüzde olarak alır veya ayarlar. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Üst pasta grafiğinin ilk diliminin açısını derece cinsinden alır veya ayarlar. |
| [get_GapWidth](./get_gapwidth/)() | Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır veya ayarlar. |
| [get_Overlap](./get_overlap/)() | Seri çubukları veya sütunlarının ne kadar üst üste geleceğinin yüzdesini alır veya ayarlar. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır veya ayarlar. |
| [get_Series](./get_series/)() | Bu seri grubuna ait serilerin bir koleksiyonunu alır. |
| [get_SeriesType](./get_seriestype/)() | Bu grupta bulunan grafik serisi türünü alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Ayarlayıcı: [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Açıklamalar


Kombinasyon grafikleri, her seri türü için ayrı bir grup içeren birden fazla grafik serisi grubu içerir.

Ayrıca, bir veya daha fazla grafik serisine ikincil eksen atamak için bir grafik serisi grubu oluşturabilirsiniz.

Daha fazla bilgi edinmek için [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

## Örnekler



Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Varsayılan oluşturulan seriyi sil.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Ayrıca çizgi tipi bir ek seri grubu oluşturun.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// İkincil X eksenini gizle.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// İkincil Y ekseninin başlığını tanımla.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Yeni seri grubuna bir seri ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
