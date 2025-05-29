---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Rotation, легко определяйте и настраивайте углы поворота для ваших фигур, повышая точность и креативность вашего дизайна.
type: docs
weight: 500
url: /ru/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует углу поворота по часовой стрелке.

```csharp
public double Rotation { get; set; }
```

## Примечания

Значение по умолчанию — 0.

## Примеры

Показывает, как вставить и повернуть изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте фигуру с изображением.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Повернуть изображение на 45 градусов по часовой стрелке.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
