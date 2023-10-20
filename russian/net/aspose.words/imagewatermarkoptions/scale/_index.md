---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words для .NET
description: ImageWatermarkOptions Scale свойство. Получает или задает масштабный коэффициент выраженный как часть изображения. Значение по умолчанию 0  auto.  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Получает или задает масштабный коэффициент, выраженный как часть изображения. Значение по умолчанию: 0 — auto. .

```csharp
public double Scale { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentOutOfRangeException | Выдает, когда аргумент выходит за пределы допустимого диапазона значений. |

## Примечания

Допустимые значения находятся в диапазоне от 0 до 65,5 включительно.

Автоматическое масштабирование означает, что водяной знак будет масштабироваться до максимальной ширины и максимальной высоты относительно полей страницы.

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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
