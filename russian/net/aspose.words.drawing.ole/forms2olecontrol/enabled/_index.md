---
title: Forms2OleControl.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words для .NET
description: Узнайте, как свойство Forms2OleControl Enabled улучшает взаимодействие с пользователем, подтверждая, активен ли элемент управления. Повысьте функциональность своего приложения!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Возврат`истинный` если элемент управления находится во включенном состоянии.

```csharp
public bool Enabled { get; }
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

* class [Forms2OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
