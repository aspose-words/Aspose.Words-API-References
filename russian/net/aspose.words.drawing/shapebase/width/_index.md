---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Width. Легко настройте ширину содержащего блока вашей фигуры для повышения гибкости и точности дизайна.
type: docs
weight: 610
url: /ru/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Возвращает или задает ширину содержащего блока фигуры.

```csharp
public double Width { get; set; }
```

## Примечания

Для фигуры верхнего уровня значение указывается в пунктах.

Для фигур в группе значение находится в координатном пространстве и единицах измерения родительской группы.

Значение по умолчанию — 0.

## Примеры

Показывает, как вставить плавающее изображение и указать его положение и размер.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Настройте свойство "RelativeHorizontalPosition" фигуры для обработки значения свойства "Left"
 // как горизонтальное расстояние фигуры в пунктах от левого края страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Установите горизонтальное расстояние фигуры от левого края страницы на 100.
shape.Left = 100;

// Используйте свойство "RelativeVerticalPosition" аналогичным образом, чтобы расположить фигуру на 80 пунктов ниже верхней части страницы.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Задайте высоту фигуры, которая автоматически масштабирует ширину для сохранения размеров.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Свойства «Bottom» и «Right» содержат нижний и правый края изображения.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

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

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
