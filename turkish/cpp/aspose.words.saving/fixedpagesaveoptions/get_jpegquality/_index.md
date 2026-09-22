---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality yöntemi"
linktitle: "get_JpegQuality"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality yöntemi. C++'da Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Html belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Açıklamalar


Yalnızca bir belge JPEG görüntüleri içerdiğinde etkili olur.

Bu özelliği, sabit sayfa biçiminde kaydederken bir belgedeki görüntülerin kalitesini almak veya ayarlamak için kullanın. Değer 0 ile 100 arasında değişebilir; 0 en düşük kaliteyi ancak maksimum sıkıştırmayı, 100 ise en yüksek kaliteyi ancak minimum sıkıştırmayı ifade eder.

Varsayılan değer 95'tir.

## Örnekler



Bir belgeyi JPEG olarak kaydederken sıkıştırmayı nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// Bu yöntemin belgeyi bir görüntüye render etme şeklini değiştirmek için
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// \"JpegQuality\" özelliğini \"10\" olarak ayarlayarak belgeyi render ederken daha güçlü sıkıştırma kullanın.
// Bu, belgenin dosya boyutunu azaltacak, ancak görüntü daha belirgin sıkıştırma artefaktları gösterecektir.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// \"JpegQuality\" özelliğini \"100\" olarak ayarlayarak belgeyi render ederken daha zayıf sıkıştırma kullanın.
// Bu, dosya boyutunun artması pahasına görüntü kalitesini artıracaktır.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Ayrıca Bakınız

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
