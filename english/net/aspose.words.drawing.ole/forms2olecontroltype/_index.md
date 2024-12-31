---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControlType enum. Enumerates types of Forms 2.0 controls in C#.
type: docs
weight: 1460
url: /net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Enumerates types of Forms 2.0 controls.

```csharp
public enum Forms2OleControlType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| OptionButton | `0` | A radio button control. |
| Label | `1` | A control that displays text. |
| Textbox | `2` | A control that allows the user to enter text. |
| CheckBox | `3` | A control that allows the user to select or deselect an option. |
| ToggleButton | `4` | A control that allows the user to toggle between two states. |
| SpinButton | `5` | A control that allows the user to increase or decrease a value. |
| ComboBox | `6` | A control that allows the user to select an item from a list. |
| Frame | `7` | A control that groups other controls. |
| MultiPage | `8` | A control that displays multiple pages of content. |
| TabStrip | `9` | A control that allows the user to switch between multiple pages of content. |
| CommandButton | `10` | A button that triggers an action when clicked. |
| Image | `11` | A control that displays an image. |
| ScrollBar | `12` | A control that allows the user to scroll through content. |
| Form | `13` | A container for other controls. |
| ListBox | `14` | A control that displays a list of items. |

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

* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
