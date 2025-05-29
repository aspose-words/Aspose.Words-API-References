---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words для .NET
description: Оптимизируйте качество JPEG в ваших HTML-документах с помощью FixedPageSaveOptions. Легко настройте свойство JpegQuality для потрясающей четкости изображения.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Возвращает или задает значение, определяющее качество изображений JPEG внутри документа HTML.

```csharp
public int JpegQuality { get; set; }
```

## Примечания

Действует только в том случае, если документ содержит изображения JPEG.

Используйте это свойство для получения или установки качества изображений внутри документа при сохранении в формате фиксированной страницы. Значение может варьироваться от 0 до 100, где 0 означает наихудшее качество, но максимальное сжатие, а 100 означает наилучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

## Примеры

Показывает, как настроить сжатие при сохранении документа в формате JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Установите свойство «JpegQuality» на «10», чтобы использовать более сильное сжатие при рендеринге документа.
// Это уменьшит размер файла документа, но на изображении будут видны более заметные артефакты сжатия.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Установите свойство «JpegQuality» на «100», чтобы использовать более слабое сжатие при визуализации документа.
// Это улучшит качество изображения за счет увеличения размера файла.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Смотрите также

* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
