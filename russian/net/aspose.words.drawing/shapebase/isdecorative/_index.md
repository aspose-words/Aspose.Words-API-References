---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words для .NET
description: ShapeBase IsDecorative свойство. Получает или задает флаг указывающий является ли фигура декоративной в документе на С#.
type: docs
weight: 240
url: /ru/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Получает или задает флаг, указывающий, является ли фигура декоративной в документе.

```csharp
public bool IsDecorative { get; set; }
```

## Примечания

Обратите внимание, что фигура не пуста.[`AlternativeText`](../alternativetext/) не может быть декоративным.

## Примеры

Показывает, как сделать фигуру декоративной.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Если "AlternativeText" не пуст, фигура не может быть декоративной.
// Вот почему наше значение изменилось на «false».
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Создаем новую фигуру как декоративную.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
