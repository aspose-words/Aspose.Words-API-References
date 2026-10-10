---
title: "Aspose::Words::ImageWatermarkOptions class"
linktitle: "ImageWatermarkOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImageWatermarkOptions sınıfı. Görüntüyle filigran eklerken belirtilebilecek seçenekleri içerir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Görüntü ile filigran eklerken belirtilebilecek seçenekleri içerir. Daha fazla bilgi edinmek için [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImageWatermarkOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Filigranın solma etkisinden sorumlu olan boolean değeri alır veya ayarlar. Varsayılan değer **true**. |
| [get_Scale](./get_scale/)() const | Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır veya ayarlar. Varsayılan değer 0 - otomatik. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Ayarlayıcı [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Ayarlayıcı [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

## Örnekler



Yerel dosya sistemindeki bir görüntüden filigran oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// ImageWatermarkOptions nesnesiyle görüntü filigranının görünümünü değiştirin,
// daha sonra bir görüntü dosyasından filigran oluştururken onu geçirin.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Görüntü eklemek için farklı seçeneklerimiz var.
// Görüntü filigranı eklemek için aşağıdaki yöntemlerden birini kullanın.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
