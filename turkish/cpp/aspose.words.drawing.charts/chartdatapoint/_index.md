---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint sınıfı"
linktitle: "ChartDataPoint"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint sınıfı. Grafik üzerindeki tek bir veri noktasının biçimlendirilmesini belirtmeye olanak tanır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Grafikte tek bir veri noktasının biçimlendirilmesini belirtmeye olanak tanır. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormat](./clearformat/)() | Bu veri noktasının biçimini temizler. Özellikler, üst seride tanımlanan varsayılan değerlere ayarlanır. |
| [get_Bubble3D](./get_bubble3d/)() override | Balon grafiğindeki balonların 3D etkisi uygulanıp uygulanmayacağını belirtir. |
| [get_Explosion](./get_explosion/)() override | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. Negatif olabilir; negatif, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir. |
| [get_Format](./get_format/)() | Bu veri noktasının dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_Index](./get_index/)() | Bu nesnenin biçimlendirme uyguladığı veri noktasının indeksi. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| [get_Marker](./get_marker/)() override | Grafik veri işaretçisini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Balon grafiğindeki balonların 3D etkisi uygulanıp uygulanmayacağını belirtir. |
| [set_Explosion](./set_explosion/)(int32_t) override | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
