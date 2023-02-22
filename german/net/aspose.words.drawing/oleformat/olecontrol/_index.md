---
title: OleFormat.OleControl
second_title: Aspose.Words für .NET-API-Referenz
description: OleFormat eigendom. erhältOleControl Objekte wenn dieses OLEObjekt ein ActiveXSteuerelement ist. Andernfalls ist diese Eigenschaft null.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

erhält`OleControl` Objekte, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null.

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../oleformat/)
* Montage [Aspose.Words](../../../)


