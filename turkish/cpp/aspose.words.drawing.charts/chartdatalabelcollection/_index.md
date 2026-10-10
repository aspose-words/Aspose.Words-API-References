---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection sınıfı. ChartDataLabel koleksiyonunu temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Bir [ChartDataLabel](../chartdatalabel/) koleksiyonunu temsil eder. Daha fazla bilgi edinmek için [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) belge makalesini ziyaret edin.

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormat](./clearformat/)() | Bu koleksiyondaki tüm [ChartDataLabel](../chartdatalabel/) öğelerinin biçimini temizler. |
| [get_Count](./get_count/)() | Bu koleksiyondaki [ChartDataLabel](../chartdatalabel/) sayısını döndürür. |
| [get_Font](./get_font/)() | Tüm serinin veri etiketlerinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Format](./get_format/)() | Veri etiketlerinin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_NumberFormat](./get_numberformat/)() | Tüm serinin veri etiketleri için sayı biçimini ayarlamayı sağlayan bir [ChartNumberFormat](../chartnumberformat/) örneği alır. |
| [get_Orientation](./get_orientation/)() | Tüm serinin veri etiketlerinin metin yönelimini alır veya ayarlar. |
| [get_Position](./get_position/)() | Veri etiketlerinin konumunu alır veya ayarlar. |
| [get_Rotation](./get_rotation/)() | Tüm serinin veri etiketlerinin döndürülmesini derece cinsinden alır veya ayarlar. |
| [get_Separator](./get_separator/)() | Tüm serinin veri etiketleri için kullanılan dize ayırıcıyı alır veya ayarlar. Varsayılan olarak virgül kullanılır; yalnızca kategori adı ve yüzde gösteren pasta grafiklerinde bunun yerine satır sonu kullanılır. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Tüm serinin veri etiketlerinde balon boyutunun gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Yalnızca Balon grafiklerinde uygulanır. Varsayılan değer **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Tüm serinin veri etiketlerinde kategori adının gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Tüm serinin veri etiketlerinde veri etiketi aralığından değerlerin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Tüm serinin veri etiketleri için veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Tüm serinin veri etiketlerinde lejand anahtarının gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Tüm serinin veri etiketlerinde yüzde değerinin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. Yalnızca Pasta grafiklerinde uygulanır. |
| [get_ShowSeriesName](./get_showseriesname/)() | Tüm serinin veri etiketleri için seri adının gösterim davranışını belirten bir Boolean döndürür veya ayarlar. Seri adını göstermek için **true**, gizlemek için **false**. Varsayılan **false**. |
| [get_ShowValue](./get_showvalue/)() | Tüm serinin veri etiketlerinde değerlerin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeks için [ChartDataLabel](../chartdatalabel/) döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/) için ayarlayıcı. |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/) için ayarlayıcı. |
| [set_Rotation](./set_rotation/)(int32_t) | [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/) için ayarlayıcı. |
| [set_Separator](./set_separator/)(const System::String\&) | [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/) için ayarlayıcı. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Tüm serinin veri etiketlerinde veri etiketi aralığından değerlerin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
