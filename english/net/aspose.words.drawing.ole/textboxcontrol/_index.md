---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Ole.TextBoxControl class to effortlessly display organized text from data or user input. Enhance your document management today!
type: docs
weight: 1510
url: /net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

The TextBox control displays text from an organized set of data or user input.

```csharp
public class TextBoxControl : MorphDataControl
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Gets or sets a background color of the control. The default value depends on a type of the control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Gets or sets a Caption property of the control. Default value is an empty string. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Gets collection of immediate child controls. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returns `true` if control is in enabled state. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Gets or sets a foreground color of the control. The default value depends on a type of the control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Gets or sets a height of the control in points. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returns `true` if the control is a [`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Gets or sets name of the ActiveX control. |
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Gets or sets a text of the control. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Gets type of Forms 2.0 control. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Gets or sets a width of the control in points. |

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

* class [MorphDataControl](../morphdatacontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
