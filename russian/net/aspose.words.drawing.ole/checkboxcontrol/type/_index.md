---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CheckBoxControl Type для Forms 2.0, открывающее универсальные возможности управления для улучшения функциональности вашего приложения.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

Получает тип элемента управления Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
