---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Ole.TextBoxControl class. The TextBox control displays text from an organized set of data or user input in C#.
type: docs
weight: 1260
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
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Gets Caption property of control. Default value is an empty string. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Gets collection of immediate child controls. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returns `true` if control is in enabled state. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returns `true` if the control is a [`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Gets or sets name of the ActiveX control. |
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Gets or sets a text of the control. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Gets type of Forms 2.0 control. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |

## Examples

Shows how to change text of the TextBox OLE control.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
```

### See Also

* class [MorphDataControl](../morphdatacontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
