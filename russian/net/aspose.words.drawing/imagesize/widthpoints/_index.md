---
title: ImageSize.WidthPoints
linktitle: WidthPoints
articleTitle: WidthPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSize WidthPoints, чтобы легко получить ширину изображения в точках — идеально для точных измерений в дизайн-проектах!
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/imagesize/widthpoints/
---
## ImageSize.WidthPoints property

Получает ширину изображения в точках. 1 точка равна 1/72 дюйма.

```csharp
public double WidthPoints { get; }
```

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

* class [ImageSize](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
