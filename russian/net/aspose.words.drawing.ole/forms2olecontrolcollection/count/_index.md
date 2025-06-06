---
title: Forms2OleControlCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Forms2OleControlCollection Count, чтобы легко получить общее количество объектов в вашей коллекции для улучшенного управления данными.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

Получает количество объектов в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как получить доступ к элементу управления OLE, встроенному в документ, и его дочерним элементам управления.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Фигуры хранят и отображают объекты OLE в теле документа.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Некоторые элементы управления OLE могут содержать дочерние элементы управления, например, тот, что в этом документе с тремя кнопками выбора.
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

* class [Forms2OleControlCollection](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
