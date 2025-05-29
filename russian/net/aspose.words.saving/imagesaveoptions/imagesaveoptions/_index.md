---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор ImageSaveOptions для сохранения изображений в универсальных форматах, таких как TIFF, PNG, BMP, JPEG, EMF, EPS, WebP и SVG. Оптимизируйте обработку изображений!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения визуализированных изображений в Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP илиSvg формат.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Может быть Tiff ,Png ,Bmp , Jpeg ,Emf ,EpsWebP илиSvg формат. |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
