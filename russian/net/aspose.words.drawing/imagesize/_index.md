---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.ImageSize — ваш основной ресурс для получения подробной информации о размере и разрешении изображений для повышения качества документов.
type: docs
weight: 1400
url: /ru/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Содержит информацию о размере и разрешении изображения.

Чтобы узнать больше, посетите[Работа с изображениями](https://docs.aspose.com/words/net/working-with-images/) документальная статья.

```csharp
public class ImageSize
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Инициализирует ширину и высоту до указанных значений в пикселях. Инициализирует разрешение до 96 точек на дюйм. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Инициализирует ширину, высоту и разрешение указанными значениями. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Получает высоту изображения в пикселях. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Получает высоту изображения в точках. 1 точка равна 1/72 дюйма. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Получает горизонтальное разрешение в DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Получает вертикальное разрешение в DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Получает ширину изображения в пикселях. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Получает ширину изображения в точках. 1 точка равна 1/72 дюйма. |

## Примеры

Показывает, как изменить размер фигуры с помощью изображения.

```csharp
// Когда мы вставляем изображение с помощью метода «InsertImage», конструктор масштабирует форму, отображающую изображение, таким образом, чтобы,
// когда мы просматриваем документ с использованием 100% масштаба в Microsoft Word, фигура отображает изображение в его реальном размере.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Изображение размером 400x400 создаст объект ImageData с размером изображения 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Если размеры фигуры соответствуют размерам данных изображения,
// тогда фигура отображает изображение в исходном размере.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Уменьшить общий размер фигуры на 50%.
shape.Width *= 0.5;

 // Коэффициенты масштабирования применяются одновременно к ширине и высоте, чтобы сохранить пропорции фигуры.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// При изменении размера фигуры размер данных изображения остается прежним.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Мы можем ссылаться на размеры данных изображения, чтобы применить масштабирование на основе размера изображения.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Смотрите также

* property [ImageSize](../imagedata/imagesize/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
