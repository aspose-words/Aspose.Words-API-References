---
title: OleFormat.OleControl
linktitle: OleControl
second_title: Aspose.Words for .NET API Reference
description: OleFormat OleControl property. Gets OleControl objects if this OLE object is an ActiveX control. Otherwise this property is null in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Gets `OleControl` objects if this OLE object is an ActiveX control. Otherwise this property is null.

```csharp
public OleControl OleControl { get; }
```

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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* namespace [Aspose.Words.Drawing](../../oleformat/)
* assembly [Aspose.Words](../../../)
