---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words для .NET
description: ShapeBase CanHaveImage свойство. Возвращаетистинный если тип фигуры позволяет фигуре иметь изображение на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Возвращает`истинный` если тип фигуры позволяет фигуре иметь изображение.

```csharp
public bool CanHaveImage { get; }
```

## Примечания

Хотя Microsoft Word имеет специальный тип фигуры для изображений, похоже, что в документах Microsoft Word любая shape , за исключением групповой фигуры, может иметь изображение, поэтому это свойство возвращает`истинный` для всех фигур, кроме[`GroupShape`](../../groupshape/).

## Примеры

Показывает, как вставлять и поворачивать изображение.

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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
