---
title: "Aspose::Words::Drawing::Fill::SetImage метод"
linktitle: "SetImage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::SetImage метод. Изменяет тип заливки на одиночное изображение в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words.drawing/fill/setimage/
---
## Fill::SetImage(const System::ArrayPtr\<uint8_t\>\&) method


Изменяет тип заливки на одиночное изображение.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Массив байтов изображения. |

## Примеры



Показывает, как установить тип заливки фигуры как изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов установки изображения.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Использование локального имени файла системы:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Загрузить файл в массив байтов:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Из потока:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Изменяет тип заливки на одиночное изображение.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий байты изображения. |

## Примеры



Показывает, как установить тип заливки фигуры как изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов установки изображения.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Использование локального имени файла системы:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Загрузить файл в массив байтов:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Из потока:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::String\&) method


Изменяет тип заливки на одиночное изображение.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Путь к файлу изображения. |

## Примеры



Показывает, как установить тип заливки фигуры как изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов установки изображения.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Использование локального имени файла системы:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Загрузить файл в массив байтов:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Из потока:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
