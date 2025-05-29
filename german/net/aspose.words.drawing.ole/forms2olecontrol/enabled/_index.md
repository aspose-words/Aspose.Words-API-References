---
title: Forms2OleControl.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „Forms2OleControl Enabled“ die Benutzerinteraktion verbessert, indem sie bestätigt, ob das Steuerelement aktiv ist. Steigern Sie die Funktionalität Ihrer App!
type: docs
weight: 40
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Rückgaben`WAHR` wenn die Steuerung aktiviert ist.

```csharp
public bool Enabled { get; }
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

* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
