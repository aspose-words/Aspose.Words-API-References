---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale metodu"
linktitle: "get_Scale"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale metodu. Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır veya ayarlar. C++'ta varsayılan değer 0 - otomattir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır veya ayarlar. Varsayılan değer 0 - otomatik.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Açıklamalar


Geçerli değerler 0 ile 65,5 arasında (her iki uç dahil).

Otomatik ölçekleme, filigranın sayfa kenar boşluklarına göre maksimum genişliğine ve maksimum yüksekliğine ölçekleneceği anlamına gelir.

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
