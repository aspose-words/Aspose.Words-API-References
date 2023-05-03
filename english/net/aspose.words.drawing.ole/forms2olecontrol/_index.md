---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Ole.Forms2OleControl class. Represents Microsoft Forms 2.0 OLE control in C#.
type: docs
weight: 1080
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
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Gets Caption property of control. Default value is an empty string. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Gets collection of immediate child controls. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returns `true` if control is in enabled state. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returns `true` if the control is a `Forms2OleControl`. |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Gets or sets name of the ActiveX control. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Gets type of Forms 2.0 control. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |

## Examples

Shows how to verify the properties of an ActiveX control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### See Also

* class [OleControl](../olecontrol/)
* namespace [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../)
