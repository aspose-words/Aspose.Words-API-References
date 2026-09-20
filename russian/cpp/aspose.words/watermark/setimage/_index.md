---
title: "Метод Aspose::Words::Watermark::SetImage"
linktitle: "SetImage"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Watermark::SetImage. Добавляет изображение в виде водяного знака в документ в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Добавляет изображение водяного знака в документ.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |

## Примеры



Показывает, как создать водяной знак из изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Измените внешний вид изображенного водяного знака с помощью объекта ImageWatermarkOptions,
// затем передайте его при создании водяного знака из файла изображения.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// У нас есть различные варианты вставки изображения.
// Используйте один из следующих методов для добавления изображенного водяного знака.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## См. также

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| изображение | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |

## Примеры



Показывает, как создать водяной знак из изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Измените внешний вид изображенного водяного знака с помощью объекта ImageWatermarkOptions,
// затем передайте его при создании водяного знака из файла изображения.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// У нас есть различные варианты вставки изображения.
// Используйте один из следующих методов для добавления изображенного водяного знака.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## См. также

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий данные изображения, отображаемого в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |

## Примеры



Показывает, как создать водяной знак из потока изображения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Измените внешний вид изображенного водяного знака с помощью объекта ImageWatermarkOptions,
// затем передайте его при создании водяного знака из файла изображения.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## См. также

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | const System::String\& | Путь к файлу изображения, отображаемому в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |

## Примеры



Показывает, как создать водяной знак из изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Измените внешний вид изображенного водяного знака с помощью объекта ImageWatermarkOptions,
// затем передайте его при создании водяного знака из файла изображения.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// У нас есть различные варианты вставки изображения.
// Используйте один из следующих методов для добавления изображенного водяного знака.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## См. также

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
