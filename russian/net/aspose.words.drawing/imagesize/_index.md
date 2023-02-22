---
title: Class ImageSize
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.ImageSize сорт. Содержит информацию о размере и разрешении изображения.
type: docs
weight: 940
url: /ru/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Содержит информацию о размере и разрешении изображения.

```csharp
public class ImageSize
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ImageSize](imagesize/#constructor)(int, int) | Инициализирует ширину и высоту заданными значениями в пикселях. Инициализирует разрешение до 96 dpi. |
| [ImageSize](imagesize/#constructor_1)(int, int, double, double) | Инициализирует ширину, высоту и разрешение заданными значениями. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Получает высоту изображения в пикселях. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Получает высоту изображения в точках. 1 пункт равен 1/72 дюйма. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Получает разрешение по горизонтали в DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Получает вертикальное разрешение в DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Получает ширину изображения в пикселях. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Получает ширину изображения в пунктах. 1 пункт равен 1/72 дюйма. |

### Примеры

Показывает, как изменить размер фигуры с изображением.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // Когда мы вставляем изображение с помощью метода «InsertImage», построитель масштабирует фигуру, отображающую изображение, так что,
            // когда мы просматриваем документ, используя масштаб 100% в Microsoft Word, фигура отображает изображение в его реальном размере.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // Изображение 400x400 создаст объект ImageData с размером изображения 300x300pt.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Если размеры фигуры совпадают с размерами данных изображения,
            // тогда фигура отображает изображение в исходном размере.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Уменьшаем общий размер фигуры на 50%.
            shape.Width *= 0.5;

             // Коэффициенты масштабирования применяются одновременно и к ширине, и к высоте, чтобы сохранить пропорции фигуры.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // Когда мы изменяем размер фигуры, размер данных изображения остается прежним.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Мы можем ссылаться на размеры данных изображения, чтобы применить масштабирование в зависимости от размера изображения.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Смотрите также

* property [ImageSize](../imagedata/imagesize/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


