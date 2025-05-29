---
title: ShapeBase.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Top. Легко управляйте положением верхнего края контейнера вашей фигуры для точной компоновки и гибкости дизайна.
type: docs
weight: 580
url: /ru/net/aspose.words.drawing/shapebase/top/
---
## ShapeBase.Top property

Возвращает или задает положение верхнего края содержащего блока фигуры.

```csharp
public double Top { get; set; }
```

## Примечания

Для фигуры верхнего уровня значение указывается в пунктах и относительно привязки фигуры.

Для фигур в группе значение находится в координатном пространстве и единицах измерения родительской группы.

Значение по умолчанию — 0.

Действует только для плавающих фигур.

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

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
