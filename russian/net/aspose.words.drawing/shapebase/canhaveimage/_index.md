---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase CanHaveImage — узнайте, как определить, поддерживает ли ваш тип фигуры изображения для повышения визуальной привлекательности!
type: docs
weight: 100
url: /ru/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Возврат`истинный` если тип фигуры позволяет фигуре иметь изображение.

```csharp
public bool CanHaveImage { get; }
```

## Примечания

Хотя в Microsoft Word есть специальный тип фигуры для изображений, похоже, что в документах Microsoft Word любая фигура shape , за исключением групповой фигуры, может иметь изображение, поэтому это свойство возвращает`истинный` для всех форм, кроме[`GroupShape`](../../groupshape/).

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
