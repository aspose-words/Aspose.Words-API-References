---
title: Forms2OleControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Forms2OleControl Type свойство. Получает тип элемента управления Forms 2.0 на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

Получает тип элемента управления Forms 2.0.

```csharp
public abstract Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
