---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words for .NET
description: OptionButtonControl Selected property. Gets or sets a boolean value indicating either this OptionButtonControl is selected or not in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Gets or sets a boolean value indicating either this [`OptionButtonControl`](../) is selected or not.

```csharp
public bool Selected { get; set; }
```

## Remarks

Note, this property allows you to select multiple items in a group of [`OptionButtonControl`](../) with the same [`GroupName`](../../forms2olecontrol/groupname/). It is up to you to take care of deselecting a previously selected item when you make this [`OptionButtonControl`](../) selected.

## Examples

Shows how to select radio button.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Deselect selected first item.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Select second option button.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### See Also

* class [OptionButtonControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
