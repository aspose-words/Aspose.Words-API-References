---
title: ShapeBase.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IsInsertRevision ShapeBase улучшает ваши документы Word, выявляя изменения, внесенные во время отслеживания. Повысьте эффективность редактирования!
type: docs
weight: 320
url: /ru/net/aspose.words.drawing/shapebase/isinsertrevision/
---
## ShapeBase.IsInsertRevision property

Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsInsertRevision { get; }
```

## Примеры

Показывает, как работать с формами исправлений.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Вставить встроенную фигуру без отслеживания изменений, в результате чего эта фигура не будет являться какой-либо ревизией.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Начать отслеживать изменения, а затем вставить другую фигуру, которая будет изменением.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Поскольку мы удалили эту фигуру, пока отслеживали изменения,
// форма сохраняется в документе и считается удаленной ревизией.
// Принятие этой правки приведет к окончательному удалению фигуры, а отклонение сохранит ее в документе.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// И мы вставили еще одну фигуру во время отслеживания изменений, поэтому эта фигура будет считаться вставленной правкой.
// Принятие этой редакции ассимилирует эту форму в документ как неревизию,
// и отклонение изменения удалит эту форму навсегда.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
