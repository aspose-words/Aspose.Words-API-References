---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IsMoveToRevision в ShapeBase расширяет возможности Microsoft Word, позволяя легко отслеживать перемещения объектов во время редактирования.
type: docs
weight: 350
url: /ru/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsMoveToRevision { get; }
```

## Примеры

Показывает, как определить формы пересмотра хода.

```csharp
// Перемещение ревизии — это перемещение элемента в теле документа путем его копирования и вставки в Microsoft Word, пока
// отслеживание изменений. Если мы включаем встроенную фигуру в такое перемещение текста, эта фигура также будет ревизией.
// Копирование и вставка или перемещение плавающих фигур не приводит к созданию изменений перемещения.
Document doc = new Document(MyDir + "Revision shape.docx");

// Перемещение ревизий состоит из пар "Переместить из" и "Переместить в". Мы переместили этот документ в одну форму,
// но пока мы не примем или не отклоним изменение хода, будет два экземпляра этой фигуры.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Это редакция «Переместить в», которая представляет собой форму в месте прибытия.
// Если мы примем ревизию, эта форма ревизии «Перейти к» исчезнет,
// и форма ревизии «Переместить из» останется.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Это «Переместить из»-редакции, которая представляет собой форму в ее исходном положении.
// Если мы примем ревизию, эта форма ревизии «Перейти из» исчезнет,
// и форма ревизии «Переместить в» останется.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
