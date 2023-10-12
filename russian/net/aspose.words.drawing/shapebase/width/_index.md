---
title: ShapeBase.Width
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает ширину содержащего блока фигуры.
type: docs
weight: 570
url: /ru/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Получает или задает ширину содержащего блока фигуры.

```csharp
public double Width { get; set; }
```

### Примечания

Для фигуры верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в координатном пространстве и единицах родительской группы.

Значение по умолчанию — 0.

### Примеры

Показывает, как вставить плавающее изображение и указать его положение и размер.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Настраиваем свойство «RelativeHorizontalPosition» фигуры для обработки значения свойства «Left».
 // как горизонтальное расстояние фигуры в пунктах от левой части страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Установите горизонтальное расстояние фигуры от левой части страницы до 100.
shape.Left = 100;

// Используйте свойство RelativeVerticalPosition аналогичным образом, чтобы расположить фигуру на 80 пунктов ниже верхнего края страницы.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Установите высоту фигуры, которая автоматически масштабирует ширину для сохранения размеров.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Свойства «Низ» и «Правый» содержат нижний и правый края изображения.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


