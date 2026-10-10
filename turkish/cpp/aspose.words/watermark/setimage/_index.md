---
title: "Aspose::Words::Watermark::SetImage yöntemi"
linktitle: "SetImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Watermark::SetImage yöntemi. Belgeye görüntü filigranı ekler (C++)."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Belgeye resim filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye resim filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | const System::SharedPtr\<System::Drawing::Image\>\& | Filigran olarak görüntülenen resim. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye resim filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Filigran olarak görüntülenen resim verilerini içeren akış. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |

## Örnekler



Bir görüntü akışından filigran oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// ImageWatermarkOptions nesnesiyle görüntü filigranının görünümünü değiştirin,
// daha sonra bir görüntü dosyasından filigran oluştururken onu geçirin.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Ayrıca Bakınız

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Belgeye resim filigranı ekler.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imagePath | const System::String\& | Filigran olarak görüntülenen resim dosyasının yolu. |
| seçenekler | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Görüntü filigranı için ek seçenekleri tanımlar. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
