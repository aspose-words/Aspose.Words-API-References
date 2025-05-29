---
title: Forms2OleControl.ChildNodes
linktitle: ChildNodes
articleTitle: ChildNodes
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChildNodes-Eigenschaft von Forms2OleControl, um mühelos auf unmittelbar untergeordnete Steuerelemente zuzugreifen und diese zu verwalten und so die Funktionalität zu erweitern.
type: docs
weight: 30
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Ruft eine Sammlung unmittelbar untergeordneter Steuerelemente ab.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

## Bemerkungen

Rückgaben`null` wenn dieses Steuerelement keine Kinder haben kann.

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

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
