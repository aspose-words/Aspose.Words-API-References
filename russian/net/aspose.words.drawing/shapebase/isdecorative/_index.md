---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words для .NET
description: Откройте для себя ShapeBase. Легко управляйте декоративными свойствами в ваших документах. Улучшите визуальную привлекательность, установив флаги для уникальных дизайнов форм.
type: docs
weight: 260
url: /ru/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Возвращает или задает флаг, указывающий, является ли фигура декоративной в документе.

```csharp
public bool IsDecorative { get; set; }
```

## Примечания

Обратите внимание, что форма не пустая[`AlternativeText`](../alternativetext/) не может быть декоративным.

## Примеры

Показывает, как сделать форму декоративной.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Если «AlternativeText» не пуст, фигура не может быть декоративной.
// Вот почему наше значение изменилось на «false».
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Создаём новую декоративную форму.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
