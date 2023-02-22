---
title: OleFormat.OleControl
second_title: Справочник по API Aspose.Words для .NET
description: OleFormat свойство. получаетOleControl объекты если этот объект OLE является элементом управления ActiveX. В противном случае это свойство равно null.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

получает`OleControl` объекты, если этот объект OLE является элементом управления ActiveX. В противном случае это свойство равно null.

```csharp
public OleControl OleControl { get; }
```

### Примеры

Показывает, как проверить свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### Смотрите также

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../oleformat/)
* сборка [Aspose.Words](../../../)


