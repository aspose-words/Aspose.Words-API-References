---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words для .NET
description: ImageSaveOptions TiffCompression свойство. Получает или задает тип сжатия применяемый при сохранении созданных изображений в формате TIFF на С#.
type: docs
weight: 180
url: /ru/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Получает или задает тип сжатия, применяемый при сохранении созданных изображений в формате TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Примечания

Действует только при сохранении в формате TIFF.

Значение по умолчанию:Lzw.

## Примеры

Показывает, как выбрать схему сжатия для применения к документу, который мы преобразуем в изображение TIFF.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Создаем объект ImageSaveOptions, который мы можем передать методу Save документа.
            // чтобы изменить способ, которым этот метод преобразует документ в изображение.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Установите для свойства «TiffCompression» значение «TiffCompression.None», чтобы не применять сжатие при сохранении,
            // что может привести к созданию очень большого выходного файла.
            // Установите для свойства «TiffCompression» значение «TiffCompression.Rle», чтобы применить сжатие RLE.
            // Установите для свойства «TiffCompression» значение «TiffCompression.Lzw», чтобы применить сжатие LZW.
            // Установите для свойства «TiffCompression» значение «TiffCompression.Ccitt3», чтобы применить сжатие CCITT3.
            // Установите для свойства «TiffCompression» значение «TiffCompression.Ccitt4», чтобы применить сжатие CCITT4.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### Смотрите также

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
