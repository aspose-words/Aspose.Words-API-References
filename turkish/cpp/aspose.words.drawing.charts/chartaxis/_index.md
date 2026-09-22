---
title: "Aspose::Words::Drawing::Charts::ChartAxis sınıfı"
linktitle: "ChartAxis"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxis sınıfı. Grafiğin eksen seçeneklerini temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Grafiğin eksen seçeneklerini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Değer ekseninin kategori eksenini kategoriler arasında kesip kesmediğini gösteren bir bayrağı alır veya ayarlar. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Zaman kategori ekseninde temsil edilen en küçük zaman birimini döndürür veya ayarlar. |
| [get_CategoryType](./get_categorytype/)() | Kategori ekseninin tipini alır veya ayarlar. |
| [get_Crosses](./get_crosses/)() | Bu eksenin dik ekseni nasıl kestiğini belirtir. |
| [get_CrossesAt](./get_crossesat/)() | Eksenin dik eksen üzerinde nerede kesildiğini belirtir. |
| [get_DisplayUnit](./get_displayunit/)() | Değer ekseni için görüntü birimlerinin ölçekleme değerini belirtir. |
| [get_Document](./get_document/)() | Üst grafiği içeren belgeyi döndürür. |
| [get_Format](./get_format/)() | Eksenin çizgi biçimlendirmesine ve işaret etiketi doldurmasına erişim sağlar. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Eksenin ana ızgara çizgilerine sahip olup olmadığını gösteren bir bayrağı alır veya ayarlar. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Eksenin yardımcı ızgara çizgilerine sahip olup olmadığını gösteren bir bayrağı alır veya ayarlar. |
| [get_Hidden](./get_hidden/)() | Bu eksenin gizli olup olmadığını gösteren bir bayrağı alır veya ayarlar. |
| [get_MajorTickMark](./get_majortickmark/)() | Ana işaret çizgilerini döndürür veya ayarlar. |
| [get_MajorUnit](./get_majorunit/)() | Ana işaret çizgileri arasındaki mesafeyi döndürür veya ayarlar. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Ana işaret çizgileri arasındaki varsayılan mesafenin kullanılacağını gösteren bir bayrağı alır veya ayarlar. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Zaman kategori eksenindeki ana işaret çizgileri için ölçek değerini döndürür veya ayarlar. |
| [get_MinorTickMark](./get_minortickmark/)() | Eksen için yardımcı işaret çizgilerini döndürür veya ayarlar. |
| [get_MinorUnit](./get_minorunit/)() | Yardımcı işaret çizgileri arasındaki mesafeyi döndürür veya ayarlar. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Yardımcı işaret çizgileri arasındaki varsayılan mesafenin kullanılacağını gösteren bir bayrağı alır veya ayarlar. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Zaman kategori eksenindeki yardımcı işaret çizgileri için ölçek değerini döndürür veya ayarlar. |
| [get_NumberFormat](./get_numberformat/)() | Eksen için sayı biçimlerini tanımlamayı sağlayan bir [ChartNumberFormat](../chartnumberformat/) nesnesi döndürür. |
| [get_ReverseOrder](./get_reverseorder/)() | Eksen değerlerinin ters sırada, yani en yüksekten en düşüğe gösterilip gösterilmeyeceğini belirten bir bayrağı döndürür veya ayarlar. |
| [get_Scaling](./get_scaling/)() | Eksenin ölçeklendirme seçeneklerine erişim sağlar. |
| [get_TickLabels](./get_ticklabels/)() | Eksen işaret işareti etiketlerinin özelliklerine erişim sağlar. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | İşaret işaretlerinin çizildiği aralığı alır veya ayarlar. |
| [get_Title](./get_title/)() | Eksen başlığı özelliklerine erişim sağlar. |
| [get_Type](./get_type/)() const | Eksenin tipini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/) için. |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/) için. |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/) için. |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/) için. |
| [set_CrossesAt](./set_crossesat/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/) için. |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/) için. |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/) için. |
| [set_Hidden](./set_hidden/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/) için. |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/) için. |
| [set_MajorUnit](./set_majorunit/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/) için. |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/) için. |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/) için. |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/) için. |
| [set_MinorUnit](./set_minorunit/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/) için. |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/) için. |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/) için. |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/) için. |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/) için. |
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
