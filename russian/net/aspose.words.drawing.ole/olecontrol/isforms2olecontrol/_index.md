---
title: OleControl.IsForms2OleControl
second_title: Справочник по API Aspose.Words для .NET
description: OleControl свойство. Возвращаетистинный если контроль представляет собойForms2OleControl .
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Возвращает`истинный` если контроль представляет собой[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public bool IsForms2OleControl { get; }
```

### Примеры

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

* class [OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../olecontrol/)
* сборка [Aspose.Words](../../../)


