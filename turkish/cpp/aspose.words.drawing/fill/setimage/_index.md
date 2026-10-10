---
title: "Aspose::Words::Drawing::Fill::SetImage yöntemi"
linktitle: "SetImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::SetImage yöntemi. C++'da doldurma türünü tek görüntüye değiştirir."
type: docs
weight: 42000
url: /tr/cpp/aspose.words.drawing/fill/setimage/
---
## Fill::SetImage(const System::ArrayPtr\<uint8_t\>\&) method


Dolgu tipini tek bir görüntüye değiştirir.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Görüntü baytları dizisi. |

## Örnekler



Şekil doldurma türünün görüntü olarak nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Yerel sistem dosya adı kullanarak:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Bir dosyayı bayt dizisine yükleyin:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Bir akıştan:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Dolgu tipini tek bir görüntüye değiştirir.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Görüntü baytlarını içeren akış. |

## Örnekler



Şekil doldurma türünün görüntü olarak nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Yerel sistem dosya adı kullanarak:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Bir dosyayı bayt dizisine yükleyin:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Bir akıştan:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::String\&) method


Dolgu tipini tek bir görüntüye değiştirir.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Görüntü dosyasının yolu. |

## Örnekler



Şekil doldurma türünün görüntü olarak nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü ayarlamanın birkaç yolu vardır.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Yerel sistem dosya adı kullanarak:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Bir dosyayı bayt dizisine yükleyin:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Bir akıştan:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
