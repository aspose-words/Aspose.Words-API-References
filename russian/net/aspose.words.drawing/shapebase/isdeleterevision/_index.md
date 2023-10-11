---
title: ShapeBase.IsDeleteRevision
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Возвращает true если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
type: docs
weight: 250
url: /ru/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsDeleteRevision { get; }
```

### Примеры

Показывает, как работать с фигурами изменений.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Вставка встроенной фигуры без отслеживания изменений, что сделает эту фигуру не какой-либо версией.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Начинаем отслеживать изменения, а затем вставляем другую фигуру, которая будет версией.
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
// форма сохраняется в документе и считается удаленной версией.
// Принятие этой версии приведет к удалению фигуры навсегда, а отклонение ее сохранит ее в документе.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// И мы вставили еще одну фигуру, отслеживая изменения, так что эта фигура будет считаться вставленной версией.
// Принятие этой редакции ассимилирует эту форму в документ как нередактированную,
// и отклонение изменения приведет к удалению этой формы навсегда.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


