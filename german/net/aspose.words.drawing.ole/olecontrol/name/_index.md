---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie die OleControl-Name-Eigenschaft, um den Namen Ihres ActiveX-Steuerelements einfach zu verwalten. Verbessern Sie die Funktionalität und optimieren Sie Ihren Entwicklungsprozess noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Ruft den Namen des ActiveX-Steuerelements ab oder legt ihn fest.

```csharp
public string Name { get; set; }
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

* class [OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
