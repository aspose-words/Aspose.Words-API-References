---
title: Width
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает ширину содержащего блока фигуры.
type: docs
weight: 510
url: /ru/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Получает или задает ширину содержащего блока фигуры.

```csharp
public double Width { get; set; }
```

### Примечания

Для формы верхнего уровня значение указывается в пунктах.

Для форм в группе значение находится в пространстве координат и единицах родительской группы.

Значение по умолчанию равно 0.

### Примеры

Показывает, как вставить плавающее изображение и указать его положение и размер.

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

* class [ShapeBase](../../shapebase)
* пространство имен [Aspose.Words.Drawing](../../shapebase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
