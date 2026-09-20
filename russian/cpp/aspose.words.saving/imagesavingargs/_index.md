---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSavingArgs class. Предоставляет данные для события ImageSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Предоставляет данные для события [ImageSaving()](../iimagesavingcallback/imagesaving/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Получает объект [ShapeBase](../../aspose.words.drawing/shapebase/), соответствующий фигуре или группе фигур, которые собираются быть сохранены. |
| [get_Document](./get_document/)() | Получает объект документа, который в данный момент сохраняется. |
| [get_ImageFileName](./get_imagefilename/)() const | Получает или задает имя файла (без пути), в который будет сохранено изображение. |
| [get_ImageStream](./get_imagestream/)() const | Позволяет указать поток, в который будет сохранено изображение. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Возвращает **true**, если текущее изображение доступно для экспорта. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения изображения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Примечания


По умолчанию, когда Aspose.Words сохраняет документ в HTML, он сохраняет каждое изображение в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Чтобы применить собственную логику генерации имен файлов изображений, используйте свойства [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) и [IsImageAvailable](./get_isimageavailable/).

Чтобы сохранять изображения в потоки вместо файлов, используйте свойство [ImageStream](./get_imagestream/).
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
