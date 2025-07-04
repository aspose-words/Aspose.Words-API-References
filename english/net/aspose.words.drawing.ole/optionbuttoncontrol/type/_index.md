---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the OptionButtonControl Type property for Forms 2.0. Learn how to enhance your forms with this essential control type feature.
type: docs
weight: 20
url: /net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Gets type of Forms 2.0 control.

```csharp
public override Forms2OleControlType Type { get; }
```

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

Assert.That(optionButton1.Type, Is.EqualTo(Forms2OleControlType.OptionButton));
Assert.That(optionButton2.Type, Is.EqualTo(Forms2OleControlType.OptionButton));

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### See Also

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
