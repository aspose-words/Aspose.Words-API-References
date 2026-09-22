---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel sınıfı"
linktitle: "ChartDataLabel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel sınıfı. Bir grafik noktasında veya trend çizgisinde veri etiketini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Bir grafik noktasında veya eğri çizgisinde veri etiketini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormat](./clearformat/)() | Bu veri etiketinin biçimini temizler. Özellikler, üst veri etiketi koleksiyonunda tanımlanan varsayılan değerlere ayarlanır. |
| [get_Font](./get_font/)() | Bu veri etiketinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Format](./get_format/)() | Veri etiketinin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_Index](./get_index/)() | İçeren öğenin dizinini belirtir. Bu dizin, öğenin ebeveynin çocuk koleksiyonundan hangisine uygulanacağını belirler. Varsayılan değer 0'dır. |
| [get_IsHidden](./get_ishidden/)() | Bu etiketin gizli olup olmadığını gösteren bir bayrağı alır/ayarlar. Varsayılan değer **false**'dur. |
| [get_IsVisible](./get_isvisible/)() | Bu veri etiketinin görüntülenecek bir şeyi varsa **true** döndürür. |
| [get_Left](./get_left/)() | Veri etiketinin, grafiğin sol kenarından veya [Position](./get_position/) özelliğiyle belirtilen konumdan, [LeftMode](./get_leftmode/) özelliğinin değerine bağlı olarak, puan cinsinden uzaklığını alır veya ayarlar. |
| [get_LeftMode](./get_leftmode/)() | [Left](./get_left/) özelliği değerinin yorumlama modunu alır veya ayarlar: veri etiketinin konumunu grafiğin sol kenarından mı yoksa [Position](./get_position/) özelliğiyle belirtilen konumdan mı ayarladığını belirler. |
| [get_NumberFormat](./get_numberformat/)() | Ebeveyn öğenin sayı biçimini döndürür. |
| [get_Orientation](./get_orientation/)() | Etiket metninin yönünü alır veya ayarlar. |
| [get_Position](./get_position/)() | Veri etiketinin konumunu alır veya ayarlar. |
| [get_Rotation](./get_rotation/)() | Etiketin derece cinsinden dönüşünü alır veya ayarlar. |
| [get_Separator](./get_separator/)() | Grafikteki veri etiketleri için kullanılan dize ayırıcıyı alır. Varsayılan değer virgüldür, yalnızca kategori adı ve yüzdeyi gösteren pasta grafiklerinde ise bunun yerine satır sonu kullanılır. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Bir grafikteki veri etiketleri için balon boyutunun gösterilip gösterilmeyeceğini belirtmeye izin verir. Yalnızca Balon grafiklerinde uygulanır. Varsayılan değer **false**'dur. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Bir grafikte veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Veri etiketleri aralığından değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Bir grafikte veri etiketleri için lejand anahtarının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Bir grafikte veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Bir grafikte veri etiketleri için seri adının görüntülenme davranışını belirten bir Boolean döndürür. **true** seri adını gösterir; **false** gizler. Varsayılan olarak **false**. |
| [get_ShowValue](./get_showvalue/)() | Değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [get_Top](./get_top/)() | Veri etiketinin grafiğin üst kenarından veya [Position](./get_position/) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını alır veya ayarlar; bu, [TopMode](./get_topmode/) özelliğinin değerine bağlıdır. |
| [get_TopMode](./get_topmode/)() | Veri etiketinin konumunu grafiğin üst kenarından mı yoksa [Position](./get_position/) özelliğiyle belirtilen konumdan mı ayarladığını belirten [Top](./get_top/) özelliği değerinin yorumlama modunu alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Bu etiketin gizli olup olmadığını gösteren bir bayrağı alır/ayarlar. Varsayılan değer **false**'dur. |
| [set_Left](./set_left/)(double) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/) için ayarlayıcı. |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/) için ayarlayıcı. |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/) için ayarlayıcı. |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/) için ayarlayıcı. |
| [set_Rotation](./set_rotation/)(int32_t) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/) için ayarlayıcı. |
| [set_Separator](./set_separator/)(const System::String\&) | Bir grafikte veri etiketleri için kullanılan dize ayırıcıyı ayarlar. Varsayılan olarak virgül kullanılır, yalnızca kategori adı ve yüzde gösteren pasta grafiklerinde ise bunun yerine satır sonu kullanılır. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/) için ayarlayıcı. |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Bir grafikte veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Veri etiketleri aralığından değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Bir grafikte veri etiketleri için lejand anahtarının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Bir grafikte veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Bir grafikte veri etiketleri için seri adının görüntülenme davranışını belirten bir Boolean ayarlar. **true** seri adını gösterir; **false** gizler. Varsayılan olarak **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer **false**. |
| [set_Top](./set_top/)(double) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/) için ayarlayıcı. |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
