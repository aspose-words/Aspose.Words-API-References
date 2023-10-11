---
title: OleFormat.Clsid
second_title: Справочник по API Aspose.Words для .NET
description: OleFormat свойство. Получает CLSID объекта OLE.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Получает CLSID объекта OLE.

```csharp
public Guid Clsid { get; }
```

### Примеры

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

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../oleformat/)
* сборка [Aspose.Words](../../../)


