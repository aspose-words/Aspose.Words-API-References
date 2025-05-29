---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.TiffCompression для оптимального сохранения файла TIFF. Выберите лучший тип сжатия для высококачественных изображений страниц без усилий.
type: docs
weight: 6430
url: /ru/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Указывает, какой тип сжатия применять при сохранении изображений страниц в файл TIFF.

```csharp
public enum TiffCompression
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Указывает на отсутствие сжатия. |
| Rle | `1` | Указывает схему сжатия RLE. |
| Lzw | `2` | Указывает схему сжатия LZW. В Java эмулируется сжатием Deflate (Zip). |
| Ccitt3 | `3` | Указывает схему сжатия CCITT3. |
| Ccitt4 | `4` | Указывает схему сжатия CCITT4. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
