---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words for .NET
description: CheckBoxControl Checked property. Gets or sets a boolean value indicating either this CheckBoxControl is checked or not. The default value is false in C#.
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
```

### See Also

* class [CheckBoxControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
