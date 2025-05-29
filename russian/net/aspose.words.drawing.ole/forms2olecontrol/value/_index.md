---
title: Forms2OleControl.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Forms2OleControl Value, отражающее состояния элементов управления. Легко управляйте значениями переключателей, 1 для отмеченного, 0 для неотмеченного. Упростите кодирование!
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка.

```csharp
public string Value { get; }
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
