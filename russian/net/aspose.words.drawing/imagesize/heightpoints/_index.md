---
title: ImageSize.HeightPoints
linktitle: HeightPoints
articleTitle: HeightPoints
second_title: Aspose.Words для .NET
description: ImageSize HeightPoints свойство. Получает высоту изображения в пунктах. 1 балл равен 1/72 дюйма на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/imagesize/heightpoints/
---
## ImageSize.HeightPoints property

Получает высоту изображения в пунктах. 1 балл равен 1/72 дюйма.

```csharp
public double HeightPoints { get; }
```

## Примеры

Показывает, как изменить размер фигуры с помощью изображения.

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

            // Когда мы вставляем изображение с помощью метода «InsertImage», построитель масштабирует фигуру, отображающую изображение, так, чтобы:
            // когда мы просматриваем документ в Microsoft Word с масштабом 100%, фигура отображает изображение в его фактическом размере.
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

             // Уменьшаем общий размер фигуры на 50%.
            shape.Width *= 0.5;

             // Коэффициенты масштабирования применяются как к ширине, так и к высоте одновременно, чтобы сохранить пропорции фигуры.
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

* class [ImageSize](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
