---
title: ShapeBase.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase DistanceLeft, которое позволяет легко настроить расстояние в пунктах между текстом документа и левым краем фигур для улучшенного управления макетом.
type: docs
weight: 140
url: /ru/net/aspose.words.drawing/shapebase/distanceleft/
---
## ShapeBase.DistanceLeft property

Возвращает или задает расстояние (в пунктах) между текстом документа и левым краем фигуры.

```csharp
public double DistanceLeft { get; set; }
```

## Примечания

Значение по умолчанию — 1/8 дюйма.

Действует только для фигур верхнего уровня.

## Примеры

Показывает, как задать расстояние обтекания для текста, окружающего фигуру.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте прямоугольник и заставьте текст плотно обтекать его границы.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Установите минимальное расстояние между фигурой и окружающим текстом 40 пунктов со всех сторон.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Переместите фигуру ближе к центру страницы, а затем поверните фигуру на 60 градусов по часовой стрелке.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Добавьте текст, который будет обтекать фигуру.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
