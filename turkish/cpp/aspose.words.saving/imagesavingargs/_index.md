---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSavingArgs sınıfı. ImageSaving() olayı için veri sağlar. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


[ImageSaving()](../iimagesavingcallback/imagesaving/) olayı için veri sağlar. Daha fazla bilgi edinmek için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class ImageSavingArgs : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Kaydedilmek üzere olan şekil veya grup şekline karşılık gelen [ShapeBase](../../aspose.words.drawing/shapebase/) nesnesini alır. |
| [get_Document](./get_document/)() | Şu anda kaydedilen belge nesnesini alır. |
| [get_ImageFileName](./get_imagefilename/)() const | Görüntünün kaydedileceği dosya adını (yol olmadan) alır veya ayarlar. |
| [get_ImageStream](./get_imagestream/)() const | Görüntünün kaydedileceği akışı belirtmeye izin verir. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Mevcut görüntü dışa aktarmaya uygun ise **true** döndürür. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Aspose.Words'un bir görüntü kaydettikten sonra akışı açık tutup tutmayacağını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/) için ayarlayıcı. |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/) için ayarlayıcı. |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Varsayılan olarak, Aspose.Words bir belgeyi HTML'ye kaydettiğinde, her resmi ayrı bir dosyaya kaydeder. Aspose.Words, belge dosya adını ve benzersiz bir numarayı kullanarak belgede bulunan her resim için benzersiz bir dosya adı oluşturur.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Resim dosya adlarını oluşturmak için kendi mantığınızı uygulamak amacıyla [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) ve [IsImageAvailable](./get_isimageavailable/) özelliklerini kullanın.

Resimleri dosyalar yerine akışlara kaydetmek için [ImageStream](./get_imagestream/) özelliğini kullanın.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
