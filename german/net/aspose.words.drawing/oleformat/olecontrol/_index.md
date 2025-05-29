---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die OleFormat OleControl-Eigenschaft für den Zugriff auf ActiveX-Steuerelemente. Nutzen Sie erweiterte Funktionen und Integration für Ihre OLE-Anwendungen.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Ruft ab`OleControl` Objekte, wenn dieses OLE-Objekt ein ActiveX-Steuerelement ist. Andernfalls ist diese Eigenschaft null.

```csharp
public OleControl OleControl { get; }
```

## Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

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

    // Beachten Sie, dass Sie für einen Frame keinen Gruppennamen festlegen können.
    checkBox.GroupName = "Aspose group name";
}
```

### Siehe auch

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
