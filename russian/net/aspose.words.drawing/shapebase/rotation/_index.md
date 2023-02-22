---
title: ShapeBase.Rotation
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Определяет угол в градусах на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке.
type: docs
weight: 430
url: /ru/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке.

```csharp
public double Rotation { get; set; }
```

### Примечания

Значение по умолчанию — 0.

### Примеры

Показывает, как вставить и повернуть изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем фигуру с изображением.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Поворот изображения на 45 градусов по часовой стрелке.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


