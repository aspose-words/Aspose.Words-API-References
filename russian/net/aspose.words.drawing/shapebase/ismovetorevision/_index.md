---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words для .NET
description: ShapeBase IsMoveToRevision свойство. Возвращаетистинный если этот объект был перемещен вставлен в Microsoft Word при включенном отслеживании изменений на С#.
type: docs
weight: 330
url: /ru/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsMoveToRevision { get; }
```

## Примеры

Показывает, как определить формы перемещения изменений.

```csharp
// Перемещение версии — это когда мы перемещаем элемент в теле документа, вырезая и вставляя его в Microsoft Word, пока
// отслеживание изменений. Если мы задействуем встроенную фигуру в такое перемещение текста, эта фигура также будет редакцией.
// Копирование и вставка или перемещение плавающих фигур не создают изменений перемещения.
Document doc = new Document(MyDir + "Revision shape.docx");

// Перемещение ревизий состоит из пар ревизий «Переместить из» и «Переместить в». Мы переместили этот документ в одну форму,
// но пока мы не примем или не отклоним редакцию перемещения, будет два экземпляра этой фигуры.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Это ревизия «Переместить в», представляющая собой фигуру в пункте назначения.
// Если мы примем редакцию, эта форма ревизии «Перейти к» исчезнет,
// и форма редакции «Переместить из» останется.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Это ревизия «Переместить из», представляющая собой фигуру в исходном месте.
// Если мы примем редакцию, эта форма редакции «Перейти из» исчезнет,
// и форма редакции «Переместить в» останется.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
