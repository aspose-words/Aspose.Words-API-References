---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Manage the TextBoxControl's text easily—get or set its content for seamless user interaction and enhanced functionality in your application.
type: docs
weight: 10
url: /net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Gets or sets a text of the control.

```csharp
public string Text { get; set; }
```

## Examples

Shows how to change text of the TextBox OLE control.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.That(textBoxControl.Text, Is.EqualTo("Aspose.Words test"));

textBoxControl.Text = "Updated text";
Assert.That(textBoxControl.Text, Is.EqualTo("Updated text"));
Assert.That(textBoxControl.Type, Is.EqualTo(Forms2OleControlType.Textbox));
```

### See Also

* class [TextBoxControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
