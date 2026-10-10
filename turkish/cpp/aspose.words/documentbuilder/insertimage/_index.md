---
title: "Aspose::Words::DocumentBuilder::InsertImage yöntemi"
linktitle: "InsertImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertImage yöntemi. Bir bayt dizisinden belgeye bir görüntü ekler. Görüntü satır içi ve %100 ölçekle C++'da eklenir."
type: docs
weight: 39000
url: /tr/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Bir bayt dizisinden bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Görüntüyü içeren bayt dizisi. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir bayt dizisinden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Aşağıda bir bayt dizisinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Bir bayt dizisinden belirtilen konum ve boyutta bir görüntü ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Görüntüyü içeren bayt dizisi. |
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



Bir bayt dizisinden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Aşağıda bir bayt dizisinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Bir bayt dizisinden satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Görüntüyü içeren bayt dizisi. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir bayt dizisinden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Aşağıda bir bayt dizisinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


**Image** nesnesinden bir görüntü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | const System::SharedPtr\<System::Drawing::Image\>\& | Belgeye eklenecek görüntü. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir nesneden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Aşağıda bir Image nesnesi örneğinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


**Image** nesnesinden belirtilen konum ve boyutta bir görüntü ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | const System::SharedPtr\<System::Drawing::Image\>\& | Belgeye eklenecek görüntü. |
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



Bir nesneden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Aşağıda bir Image nesnesi örneğinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


**Image** nesnesinden satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | const System::SharedPtr\<System::Drawing::Image\>\& | Belgeye eklenecek görüntü. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir nesneden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Aşağıda bir Image nesnesi örneğinden görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Bir akıştan bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Görüntüyü içeren akış. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir akıştan belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Aşağıda bir akıştan görüntü eklemenin üç yolu verilmiştir.
    // 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Özel boyutlarda satır içi şekil:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Özel boyutlarda yüzen şekil:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Bir akıştan bir görüntü içeren şekil belgeye eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Bir akıştan belirtilen konum ve boyutta bir görüntü ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Görüntüyü içeren akış. |
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



Bir akıştan belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Aşağıda bir akıştan görüntü eklemenin üç yolu verilmiştir.
    // 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Özel boyutlarda satır içi şekil:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Özel boyutlarda yüzen şekil:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Bir akıştan satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Görüntüyü içeren akış. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir akıştan belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Aşağıda bir akıştan görüntü eklemenin üç yolu verilmiştir.
    // 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 -  Özel boyutlarda satır içi şekil:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 -  Özel boyutlarda yüzen şekil:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Bir dosya veya URL'den bir görüntüyü belgeye ekler. Görüntü satır içi ve %100 ölçekle eklenir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntüyü içeren dosya. Geçerli herhangi bir yerel veya uzak URI olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu aşırı yükleme, uzak bir URI belirttiğinizde görüntüyü belgeye eklemeden önce otomatik olarak indirir.

Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Yerel dosya sisteminden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda yerel sistem dosya adından görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Hangi görüntünün ekleneceğini belirlemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words, svgBlip uzantısıyla SVG görüntüsünü belgeye PNG olarak ekler
// orijinal vektör SVG görüntü temsilini içeren.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words, eski format için Microsoft Word'ün yaptığı gibi SVG görüntüsünü belgeye PNG olarak ekler
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words, görüntüyü vektör temsili olarak tutmak için SVG görüntüsünü belgeye EMF metafile olarak ekler.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Belgeye gif görüntüsü eklemenin nasıl yapılacağını gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Gif görüntüsünü yol veya bayt dizisi kullanarak ekleyebiliriz.
// Bu, yalnızca DocumentBuilder Word 2010 veya daha yeni bir sürüme optimize edilmişse çalışır.
// Not: görüntü baytlarına erişim, Gif'in Png'ye dönüştürülmesine neden olur.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Belgeye bir görüntülü şekil eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belge oluşturucunun "InsertShape" metodunun iki konumu aşağıdadır
// şeklin göstereceği görüntüyü sağlayabilir.
// 1 -  Bir görüntü dosyasının yerel dosya sistemi dosya adını geçirin:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Bir görüntüyü işaret eden bir URL'yi geçirin.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Sayfanın ortasına yüzen bir görüntünün nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Üst üste gelen metnin arkasında görünecek bir yüzen görüntü ekleyin ve sayfanın ortasına hizalayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


WebP görüntüsü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Bir dosya veya URL'den belirtilen konum ve boyutta bir görüntü ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntüyü içeren dosya. |
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



Bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir görüntüyü sağlayıp ardından yüzen bir şekil olarak eklemek için belge oluşturucu kullanmanın iki yolu vardır.
// 1 -  Yerel dosya sistemindeki bir dosyadan:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Bir URL'den:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Görüntünün boyutlarını koruyarak yerel dosya sisteminden bir görüntüyü belgeye eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// InsertImage metodu, iletilen görüntüyü görüntü verisi içinde içeren bir yüzen şekil oluşturur.
// Şeklin boyutlarını bu metoda geçirerek belirtebiliriz.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Negatif değerleri istenen boyutlar olarak geçirmek, otomatik olarak tanımlar
// şeklin boyutlarını görüntüsünün boyutlarına göre.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Yerel dosya sisteminden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda yerel sistem dosya adından görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Bir dosya veya URL'den satır içi bir görüntüyü belgeye ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntüyü içeren dosya. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Yerel dosya sisteminden belgeye bir görüntü eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda yerel sistem dosya adından görüntü eklemenin üç yolu verilmiştir.
// 1 -  Görüntünün özgün boyutlarına dayalı varsayılan boyutta satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 -  Özel boyutlarda satır içi şekil:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 -  Özel boyutlarda yüzen şekil:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
