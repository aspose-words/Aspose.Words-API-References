---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase IsDeleteRevision и узнайте, как оно указывает на удаление объекта в Microsoft Word с включенным отслеживанием изменений для улучшенного управления документами.
type: docs
weight: 270
url: /ru/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsDeleteRevision { get; }
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
