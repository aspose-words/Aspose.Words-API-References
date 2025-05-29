---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words для .NET
description: Оптимизируйте изображения TIFF с помощью свойства ImageSaveOptions TiffCompression, позволяющего выбрать наилучший метод сжатия для получения качественных результатов.
type: docs
weight: 180
url: /ru/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Возвращает или задает тип сжатия, применяемый при сохранении созданных изображений в формате TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Примечания

Действует только при сохранении в формате TIFF.

Значение по умолчанию:Lzw.

## Примеры

Показывает, как выбрать схему сжатия для применения к документу, который мы конвертируем в изображение TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Установите свойство "TiffCompression" на "TiffCompression.None", чтобы не применять сжатие при сохранении,
// что может привести к очень большому выходному файлу.
// Установите свойство "TiffCompression" на "TiffCompression.Rle", чтобы применить сжатие RLE
// Установите свойство "TiffCompression" на "TiffCompression.Lzw", чтобы применить сжатие LZW.
// Установите свойство "TiffCompression" на "TiffCompression.Ccitt3", чтобы применить сжатие CCITT3.
// Установите свойство "TiffCompression" на "TiffCompression.Ccitt4", чтобы применить сжатие CCITT4.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Смотрите также

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
