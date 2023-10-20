---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words для .NET
description: OleFormat OleControl свойство. ПолучаетOleControl объекты если этот объект OLE является элементом управления ActiveX. В противном случае это свойство имеет значение null на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Получает`OleControl` объекты, если этот объект OLE является элементом управления ActiveX. В противном случае это свойство имеет значение null.

```csharp
public OleControl OleControl { get; }
```

## Примеры

Показывает, как проверить свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Обратите внимание, что вы не можете установить GroupName для кадра.
    checkBox.GroupName = "Aspose group name";
}
```

### Смотрите также

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
