---
title: Name
second_title: Справочник по API Aspose.Words для .NET
description: Получает имя элемента управления ActiveX.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Получает имя элемента управления ActiveX.

```csharp
public string Name { get; }
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

* class [OleControl](../../olecontrol)
* пространство имен [Aspose.Words.Drawing.Ole](../../olecontrol)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->