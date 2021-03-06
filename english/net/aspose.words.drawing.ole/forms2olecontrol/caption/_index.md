---
title: Caption
second_title: Aspose.Words for .NET API Reference
description: Gets Caption property of control. Default value is an empty string.
type: docs
weight: 10
url: /net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Gets Caption property of control. Default value is an empty string.

```csharp
public string Caption { get; }
```

## Examples

Shows how to verify the properties of an ActiveX control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

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

* class [Forms2OleControl](../../forms2olecontrol)
* namespace [Aspose.Words.Drawing.Ole](../../forms2olecontrol)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
