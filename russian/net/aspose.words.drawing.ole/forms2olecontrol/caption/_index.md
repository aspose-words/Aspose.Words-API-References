---
title: Forms2OleControl.Caption
second_title: Справочник по API Aspose.Words для .NET
description: Forms2OleControl свойство. Получает свойство Caption элемента управления. Значение по умолчанию  пустая строка.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Получает свойство Caption элемента управления. Значение по умолчанию — пустая строка.

```csharp
public string Caption { get; }
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

* class [Forms2OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* сборка [Aspose.Words](../../../)


