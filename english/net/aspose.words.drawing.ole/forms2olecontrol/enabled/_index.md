---
title: Forms2OleControl.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words for .NET
description: Discover how the Forms2OleControl Enabled property enhances user interaction by confirming if the control is active. Boost your app's functionality!
type: docs
weight: 40
url: /net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Returns `true` if control is in enabled state.

```csharp
public bool Enabled { get; }
```

## Examples

Shows how to verify the properties of an ActiveX control.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.That(oleControl.Name, Is.EqualTo("CheckBox1"));

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.That(checkBox.Caption, Is.EqualTo("First"));
    Assert.That(checkBox.Value, Is.EqualTo("0"));
    Assert.That(checkBox.Enabled, Is.EqualTo(true));
    Assert.That(checkBox.Type, Is.EqualTo(Forms2OleControlType.CheckBox));
    Assert.That(checkBox.ChildNodes, Is.EqualTo(null));
    Assert.That(checkBox.GroupName, Is.EqualTo(string.Empty));

    // Note, that you can't set GroupName for a Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### See Also

* class [Forms2OleControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
