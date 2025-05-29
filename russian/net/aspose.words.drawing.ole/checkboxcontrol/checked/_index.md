---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CheckBoxControl Checked, легко управляйте состояниями флажков с помощью простого логического значения. Значение по умолчанию — false для оптимального управления.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Возвращает или задает логическое значение, указывающее, что это[`CheckBoxControl`](../) проверено или нет. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool Checked { get; set; }
```

## Примеры

Показывает, как изменить состояние элемента управления CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Смотрите также

* class [CheckBoxControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
