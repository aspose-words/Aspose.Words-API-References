---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint arayüzü"
linktitle: "IChartDataPoint"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint arayüzü. C++'ta grafikteki tek bir veri noktasının özelliklerini içerir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Grafikteki tek bir veri noktasının özelliklerini içerir.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Balon grafiğindeki balonların 3D etkisi uygulanıp uygulanmayacağını belirtir. |
| virtual [get_Explosion](./get_explosion/)() | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. Negatif olabilir; negatif, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| virtual [get_Marker](./get_marker/)() | Bir veri işaretçisi belirtir. İşaretçi istenildiğinde otomatik olarak oluşturulur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Değer negatifse, üst öğenin renklerini tersine çevirip çevirmesi gerektiğini belirtir. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
