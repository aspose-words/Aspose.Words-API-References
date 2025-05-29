---
title: OleControl.IsForms2OleControl
linktitle: IsForms2OleControl
articleTitle: IsForms2OleControl
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsForms2OleControl класса OleControl, которое определяет, является ли ваш элемент управления Forms2OleControl, что повышает эффективность разработки.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Возврат`истинный` если контроль - это[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public bool IsForms2OleControl { get; }
```

## Примеры

Показывает, как проверить свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Обратите внимание, что вы не можете задать GroupName для фрейма.
    checkBox.GroupName = "Aspose group name";
}
```

### Смотрите также

* class [OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
