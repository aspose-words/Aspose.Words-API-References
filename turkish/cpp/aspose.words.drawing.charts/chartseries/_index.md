---
title: "Aspose::Words::Drawing::Charts::ChartSeries sınıfı"
linktitle: "ChartSeries"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries sınıfı. Grafik serisi özelliklerini temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Grafik serisi özelliklerini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Belirtilen X değerini grafik serisine ekler. Seri Y değerlerini ve balon boyutlarını destekliyorsa, X değeri için bunlar boş olacaktır. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Belirtilen X ve Y değerlerini grafik serisine ekler. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Belirtilen X değeri, Y değeri ve balon boyutunu grafik serisine ekler. |
| [Clear](./clear/)() | Grafik serisindeki tüm veri değerlerini kaldırır. Tüm bireysel veri noktalarının ve veri etiketlerinin biçimi temizlenir. |
| [ClearValues](./clearvalues/)() | Grafik serisindeki tüm veri değerlerini, veri noktalarının ve veri etiketlerinin biçimini koruyarak kaldırır. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Belirtilen dizine sahip veri noktasından varsayılan veri noktası biçimini kopyalar. |
| [get_Bubble3D](./get_bubble3d/)() override | Balon grafiğindeki balonların 3D etkisi uygulanıp uygulanmayacağını belirtir. |
| [get_BubbleSizes](./get_bubblesizes/)() | Bu grafik serisi için balon boyutlarının bir koleksiyonunu alır. |
| [get_DataLabels](./get_datalabels/)() | Tüm seri için veri etiketlerinin ayarlarını belirtir. |
| [get_DataPoints](./get_datapoints/)() const | Bu serideki tüm veri noktaları için biçimlendirme nesnelerinin bir koleksiyonunu döndürür. |
| [get_Explosion](./get_explosion/)() override | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. Negatif olabilir; negatif, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir. |
| [get_Format](./get_format/)() | Serinin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Seri için veri etiketlerinin görüntülenip görüntülenmeyeceğini gösteren bir bayrağı alır veya ayarlar. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| [get_LegendEntry](./get_legendentry/)() | Bu grafik serisi için bir lejand girdisi alır. |
| [get_Marker](./get_marker/)() override | Bir veri işaretçisi belirtir. İşaretçi istenildiğinde otomatik olarak oluşturulur. |
| [get_Name](./get_name/)() | Serinin adını alır, ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur. Varsayılan olarak, bir indeks eklenmiş Series döndürür. |
| [get_SeriesType](./get_seriestype/)() | Bu grafik serisinin tipini alır. |
| [get_Smooth](./get_smooth/)() const | Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir. |
| [get_XValues](./get_xvalues/)() | Bu grafik serisi için X değerlerinin bir koleksiyonunu alır. |
| [get_YValues](./get_yvalues/)() | Bu grafik serisi için Y değerlerinin bir koleksiyonunu alır. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Belirtilen X değerini belirtilen indekste grafik serisine ekler. Seri Y değerlerini ve baloncuk boyutlarını destekliyorsa, X değeri için bunlar boş olur. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Belirtilen X ve Y değerlerini belirtilen indekste grafik serisine ekler. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Belirtilen X değeri, Y değeri ve baloncuk boyutunu belirtilen indekste grafik serisine ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Destekleniyorsa, belirtilen indekste grafik serisinden X değeri, Y değeri ve baloncuk boyutunu kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Ayarlayıcı için [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. Negatif olabilir; negatif, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Ayarlayıcı için [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| [set_Name](./set_name/)(const System::String\&) | Serinin adını ayarlar, ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur. Varsayılan olarak, bir indeks eklenmiş Series döndürür. |
| [set_Smooth](./set_smooth/)(bool) | Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
