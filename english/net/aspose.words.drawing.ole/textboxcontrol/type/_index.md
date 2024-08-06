---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: TextBoxControl Type property. Gets type of Forms 2.0 control in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Gets type of Forms 2.0 control.

```csharp
public override Forms2OleControlType Type { get; }
```

## Examples

Shows how to change text of the TextBox OLE control.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### See Also

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
