---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsWashout в ImageWatermarkOptions. Управляйте эффектом размытия вашего водяного знака без усилий с помощью этой простой логической настройки.
type: docs
weight: 20
url: /ru/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Возвращает или задает логическое значение, которое отвечает за эффект размытия водяного знака. Значение по умолчанию:`истинный` .

```csharp
public bool IsWashout { get; set; }
```

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // У нас есть разные варианты вставки изображения:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Смотрите также

* class [ImageWatermarkOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
