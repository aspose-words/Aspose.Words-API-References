---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metodu"
linktitle: "InsertOnlineVideo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metodu. Bir çevrimiçi video nesnesini belgeye ekler ve C++'da belirtilen boyuta ölçeklendirir."
type: docs
weight: 43000
url: /tr/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | const System::String\& | Videonun URL'si. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| left | double | Köken noktasından görüntünün sol tarafına kadar olan mesafe puan cinsinden. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| üst | double | Köken noktasından görüntünün üst tarafına kadar olan mesafe puan cinsinden. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin görüntünün etrafında nasıl sarılacağını belirtir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

Aşağıdaki kaynaklardan çevrimiçi video ekleme desteklenir:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Çevrimiçi videonuz doğru görüntülenmiyorsa, özel gömülü html kodu kabul eden [InsertOnlineVideo()](../) yöntemini kullanın.

Video gömme kodu sağlayıcılar arasında değişebilir, ayrıntılar için seçtiğiniz ilgili sağlayıcıyla iletişime geçin.

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | const System::String\& | Videonun URL'si. |
| videoEmbedCode | const System::String\& | Video için gömme kodu. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Küçük resim görüntüsü baytları. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| left | double | Köken noktasından görüntünün sol tarafına kadar olan mesafe puan cinsinden. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| üst | double | Köken noktasından görüntünün üst tarafına kadar olan mesafe puan cinsinden. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin görüntünün etrafında nasıl sarılacağını belirtir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Özel bir küçük resimle belgeye çevrimiçi video eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Aşağıda, özel bir küçük resimle bir şekil oluşturmanın iki yolu verilmiştir; bu, çevrimiçi bir videoya bağlanır.
        // Microsoft Word'de şekle tıkladığımızda oynatılacak.
        // 1 -  Oluşturucunun düğüm ekleme imlecinde satır içi bir şekil ekleyin:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Yüzen bir şekil ekleyin:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | const System::String\& | Videonun URL'si. |
| videoEmbedCode | const System::String\& | Video için gömme kodu. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Küçük resim görüntüsü baytları. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Özel bir küçük resimle belgeye çevrimiçi video eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Aşağıda, özel bir küçük resimle bir şekil oluşturmanın iki yolu verilmiştir; bu, çevrimiçi bir videoya bağlanır.
        // Microsoft Word'de şekle tıkladığımızda oynatılacak.
        // 1 -  Oluşturucunun düğüm ekleme imlecinde satır içi bir şekil ekleyin:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Yüzen bir şekil ekleyin:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | const System::String\& | Videonun URL'si. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

Aşağıdaki kaynaklardan çevrimiçi video ekleme desteklenir:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Çevrimiçi videonuz doğru görüntülenmiyorsa, özel gömülü html kodu kabul eden [InsertOnlineVideo()](../) yöntemini kullanın.

Video gömme kodu sağlayıcılar arasında değişebilir, ayrıntılar için seçtiğiniz ilgili sağlayıcıyla iletişime geçin.

## Örnekler



Bir URL kullanarak çevrimiçi bir videoyu belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Şekle tıklayarak videoyu Microsoft Word'den izleyebiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
