---
title: "Aspose::Words::ImageWatermarkOptions::get_IsWashout yöntemi"
linktitle: "get_IsWashout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImageWatermarkOptions::get_IsWashout yöntemi. Filigranın solma etkisinden sorumlu olan bir Boolean değerini alır veya ayarlar. Varsayılan değer C++'ta true'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Filigranın solma etkisinden sorumlu olan boolean değeri alır veya ayarlar. Varsayılan değer **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
