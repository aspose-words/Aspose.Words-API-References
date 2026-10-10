---
title: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions yapıcı"
linktitle: "ImageSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions yapıcı. C++'ta işlenmiş görüntüleri Tiff, Png, Bmp, Jpeg, Emf, Eps, WebP veya Svg formatında kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


Bu sınıfın, işlenmiş görüntüleri [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) veya [Svg](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilecek yeni bir örneğini başlatır.

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Şu formatlar olabilir: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) veya [Svg](../../../aspose.words/saveformat/) format. |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
