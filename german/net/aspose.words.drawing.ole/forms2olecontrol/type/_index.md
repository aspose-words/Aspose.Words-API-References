---
title: Forms2OleControl.Type
second_title: Aspose.Words für .NET-API-Referenz
description: Forms2OleControl eigendom. Ruft den Typ des Forms 2.0Steuerelements ab.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/type/
---
## Forms2OleControl.Type property

Ruft den Typ des Forms 2.0-Steuerelements ab.

```csharp
public abstract Forms2OleControlType Type { get; }
```

### Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Beachten Sie, dass Sie GroupName nicht für einen Frame festlegen können.
    checkBox.GroupName = "Aspose group name";
}
```

### Siehe auch

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* Montage [Aspose.Words](../../../)


