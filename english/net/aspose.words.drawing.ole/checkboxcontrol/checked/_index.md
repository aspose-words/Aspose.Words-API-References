---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words for .NET
description: Discover the CheckBoxControl Checked property, easily manage checkbox states with a simple boolean value. Default is false for optimal control.
type: docs
weight: 10
url: /net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Gets or sets a boolean value indicating either this [`CheckBoxControl`](../) is checked or not. The default value is `false`.

```csharp
public bool Checked { get; set; }
```

## Examples

Shows how to change state of the CheckBox control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.That(checkBoxControl.Checked, Is.EqualTo(true));
Assert.That(checkBoxControl.Type, Is.EqualTo(Forms2OleControlType.CheckBox));
```

### See Also

* class [CheckBoxControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
