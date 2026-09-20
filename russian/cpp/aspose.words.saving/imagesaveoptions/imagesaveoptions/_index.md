---
title: "Конструктор Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions"
linktitle: "ImageSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions. Инициализирует новый экземпляр этого класса, который может использоваться для сохранения отрисованных изображений в форматах Tiff, Png, Bmp, Jpeg, Emf, Eps, WebP или Svg в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


Инициализирует новый экземпляр этого класса, который может использоваться для сохранения отрисованных изображений в форматах [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../) или [Svg](../../../aspose.words/saveformat/) .

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Может быть в формате [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/)[WebP](../) или [Svg](../../../aspose.words/saveformat/). |

## Примеры



Показывает, как настроить сжатие при сохранении документа в формате JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Установите свойство "JpegQuality" в "10", чтобы использовать более сильное сжатие при рендеринге документа.
// Это уменьшит размер файла документа, но изображение будет показывать более заметные артефакты сжатия.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Установите свойство "JpegQuality" в "100", чтобы использовать более слабое сжатие при рендеринге документа.
// Это улучшит качество изображения за счёт увеличения размера файла.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
