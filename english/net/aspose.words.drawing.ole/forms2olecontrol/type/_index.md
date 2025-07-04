---
title: Forms2OleControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the Forms2OleControl Type property to easily retrieve the type of Forms 2.0 controls, enhancing your application's functionality and efficiency.
type: docs
weight: 80
url: /net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

Gets type of Forms 2.0 control.

```csharp
public abstract Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* namespace [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assembly [Aspose.Words](../../../)
