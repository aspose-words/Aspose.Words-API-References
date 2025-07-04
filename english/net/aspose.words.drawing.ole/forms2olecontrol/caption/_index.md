---
title: Forms2OleControl.Caption
linktitle: Caption
articleTitle: Caption
second_title: Aspose.Words for .NET
description: Discover the Forms2OleControl Caption property to easily customize your control's title. Enhance user experience with this simple, effective feature.
type: docs
weight: 20
url: /net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Gets or sets a Caption property of the control. Default value is an empty string.

```csharp
public string Caption { get; set; }
```

## Examples

Shows how to set caption for ActiveX control.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl() { Caption = "Button caption" };
Shape shape = builder.InsertForms2OleControl(button1);
Assert.That(button1.Caption, Is.EqualTo("Button caption"));
```

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
