---
title: OleControl.Name
second_title: Aspose.Words für .NET-API-Referenz
description: OleControl eigendom. Ruft den Namen des ActiveXSteuerelements ab.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Ruft den Namen des ActiveX-Steuerelements ab.

```csharp
public string Name { get; }
```

### Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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

### Siehe auch

* class [OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../olecontrol/)
* Montage [Aspose.Words](../../../)


