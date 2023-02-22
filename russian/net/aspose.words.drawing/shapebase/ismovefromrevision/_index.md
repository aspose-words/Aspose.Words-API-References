---
title: ShapeBase.IsMoveFromRevision
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Возвращает истинный если этот объект был перемещен удален в Microsoft Word при включенном отслеживании изменений.
type: docs
weight: 310
url: /ru/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Возвращает **истинный** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsMoveFromRevision { get; }
```

### Примеры

Показывает, как идентифицировать формы изменений перемещения.

```csharp
// Перемещение ревизии — это когда мы перемещаем элемент в теле документа, вырезая и вставляя его в Microsoft Word, в то время как
// отслеживание изменений. Если мы задействуем встроенную фигуру в таком перемещении текста, эта фигура также будет ревизией.
// Копирование и вставка или перемещение плавающих фигур не создает изменений перемещения.
Document doc = new Document(MyDir + "Revision shape.docx");

// Перемещение ревизий состоит из пар ревизий «Переместить из» и «Переместить в». Мы перемещались в этом документе в одной форме,
// но пока мы не примем или не отклоним ревизию перемещения, будет два экземпляра этой формы.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Это ревизия "Move to", то есть фигура в месте назначения.
// Если мы примем ревизию, эта форма ревизии «Переместить в» исчезнет,
// и форма ревизии "Переместить из" останется.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Это ревизия «Переместить из», то есть фигура в исходном положении.
// Если мы примем ревизию, эта форма ревизии «Переместить из» исчезнет,
// и форма ревизии «Переместить в» останется.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


