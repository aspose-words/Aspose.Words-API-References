---
title: ShapeBase.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words для .NET
description: ShapeBase Top свойство. Получает или задает положение верхнего края содержащего блока фигуры на С#.
type: docs
weight: 540
url: /ru/net/aspose.words.drawing/shapebase/top/
---
## ShapeBase.Top property

Получает или задает положение верхнего края содержащего блока фигуры.

```csharp
public double Top { get; set; }
```

## Примечания

Для фигуры верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в координатном пространстве и единицах родительской группы.

Значение по умолчанию — 0.

Имеет эффект только для плавающих фигур.

## Примеры

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

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
