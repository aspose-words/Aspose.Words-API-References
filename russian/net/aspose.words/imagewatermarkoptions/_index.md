---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.ImageWatermarkOptions. Настройте водяные знаки на изображениях без особых усилий с помощью универсальных опций для улучшенного представления документов.
type: docs
weight: 3670
url: /ru/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Содержит параметры, которые можно указать при добавлении водяного знака с изображением.

Чтобы узнать больше, посетите[Работа с водяным знаком](https://docs.aspose.com/words/net/working-with-watermark/) документальная статья.

```csharp
public class ImageWatermarkOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Возвращает или задает логическое значение, которое отвечает за эффект размытия водяного знака. Значение по умолчанию:`истинный` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Возвращает или задает коэффициент масштабирования, выраженный как дробь изображения. Значение по умолчанию 0 - auto. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
