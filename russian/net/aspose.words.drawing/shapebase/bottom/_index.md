---
title: ShapeBase.Bottom
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает положение нижнего края содержащего блока фигуры.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Получает положение нижнего края содержащего блока фигуры.

```csharp
public double Bottom { get; }
```

### Примечания

Для фигуры верхнего уровня значение указывается в пунктах и относительно привязки формы.

Для фигур в группе значение находится в координатном пространстве и единицах родительской группы.

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

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


