---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl class. Represents Microsoft Forms 2.0 OLE control in C#.
type: docs
weight: 1290
url: /net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Represents Microsoft Forms 2.0 OLE control.

To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) documentation article.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Gets or sets a background color of the control. The default value depends on a type of the control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Gets Caption property of control. Default value is an empty string. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Gets collection of immediate child controls. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returns `true` if control is in enabled state. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Gets or sets a foreground color of the control. The default value depends on a type of the control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Gets or sets a height of the control in points. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returns `true` if the control is a `Forms2OleControl`. |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Gets or sets name of the ActiveX control. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Gets type of Forms 2.0 control. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Gets or sets a width of the control in points. |

## Examples

Shows how to verify the properties of an ActiveX control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Note, that you can't set GroupName for a Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### See Also

* class [OleControl](../olecontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
