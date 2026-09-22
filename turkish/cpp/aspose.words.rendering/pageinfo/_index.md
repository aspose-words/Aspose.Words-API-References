---
title: "Aspose::Words::Rendering::PageInfo sınıfı"
linktitle: "PageInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::PageInfo sınıfı. Belirli bir belge sayfası hakkında bilgi temsil eder. Daha fazla bilgi için C++'daki belgeler makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Belirli bir belge sayfası hakkında bilgi temsil eder. Daha fazla bilgi için, [Rendering](https://docs.aspose.com/words/cpp/rendering/) dokümantasyon makalesini ziyaret edin.

```cpp
class PageInfo : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Colored](./get_colored/)() | Sayfa renkli içerik içeriyorsa **true** döndürür. |
| [get_HeightInPoints](./get_heightinpoints/)() | Sayfanın yüksekliğini nokta cinsinden alır. |
| [get_Landscape](./get_landscape/)() const | Belgede bu sayfa için belirtilen sayfa yönelimi yataysa **true** döndürür. |
| [get_PaperSize](./get_papersize/)() | Kağıt boyutunu enum olarak alır. |
| [get_PaperTray](./get_papertray/)() const | Belgede belirtilen bu sayfa için kağıt tepsisini (bin) alır. Değer uygulamaya (yazıcıya) özgüdür. |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Sayfa boyutunu nokta cinsinden alır. |
| [get_WidthInPoints](./get_widthinpoints/)() | Sayfanın genişliğini nokta cinsinden alır. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için sayfa boyutunu piksel cinsinden hesaplar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu nesne tarafından döndürülen sayfa genişliği ve yüksekliği, sayfanın "son" boyutunu temsil eder; örneğin zaten doğru yönelime göre döndürülmüşlerdir.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
