---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality метод"
linktitle: "get_JpegQuality"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality метод. Получает или задает значение, определяющее качество JPEG‑изображений внутри HTML‑документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/fixedpagesaveoptions/get_jpegquality/
---
## FixedPageSaveOptions::get_JpegQuality method


Получает или задает значение, определяющее качество JPEG‑изображений в HTML‑документе.

```cpp
int32_t Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality() const
```

## Примечания


Имеет эффект только когда документ содержит JPEG‑изображения.

Используйте это свойство, чтобы получить или задать качество изображений внутри документа при сохранении в формате фиксированной страницы. Значение может варьироваться от 0 до 100, где 0 означает наихудшее качество, но максимальное сжатие, а 100 — наилучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

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

* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
