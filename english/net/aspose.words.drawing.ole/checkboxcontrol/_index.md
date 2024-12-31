---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Ole.CheckBoxControl class. The CheckBox control toggles a value in C#.
type: docs
weight: 1420
url: /net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

The CheckBox control toggles a value.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Gets or sets a background color of the control. The default value depends on a type of the control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Gets or sets a Caption property of the control. Default value is an empty string. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Gets or sets a boolean value indicating either this `CheckBoxControl` is checked or not. The default value is `false`. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Gets collection of immediate child controls. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returns `true` if control is in enabled state. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Gets or sets a foreground color of the control. The default value depends on a type of the control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Gets or sets a height of the control in points. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returns `true` if the control is a [`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Gets or sets name of the ActiveX control. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Gets type of Forms 2.0 control. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Gets or sets a width of the control in points. |

## Remarks

It has three possible states: selected, cleared, and neither selected nor cleared, meaning a combination of on and off states.

## Examples

Shows how to change state of the CheckBox control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### See Also

* class [MorphDataControl](../morphdatacontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
