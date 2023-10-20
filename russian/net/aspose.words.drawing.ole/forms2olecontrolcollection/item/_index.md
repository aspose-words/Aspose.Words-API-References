---
title: Forms2OleControlCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Forms2OleControlCollection Item свойство. ПолучаетForms2OleControl объект по указанному индексу на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.ole/forms2olecontrolcollection/item/
---
## Forms2OleControlCollection indexer

Получает[`Forms2OleControl`](../../forms2olecontrol/) объект по указанному индексу.

```csharp
public Forms2OleControl this[int index] { get; }
```

## Примеры

Показывает, как получить доступ к элементу управления OLE, встроенному в документ, и его дочерним элементам управления.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Фигуры хранят и отображают объекты OLE в теле документа.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Некоторые элементы управления OLE могут содержать дочерние элементы управления, например, в этом документе с тремя кнопками параметров.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Смотрите также

* class [Forms2OleControl](../../forms2olecontrol/)
* class [Forms2OleControlCollection](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
