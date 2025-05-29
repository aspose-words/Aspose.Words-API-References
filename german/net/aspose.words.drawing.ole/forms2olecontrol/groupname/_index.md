---
title: Forms2OleControl.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Forms2OleControl GroupName-Eigenschaft die Benutzerfreundlichkeit durch die mühelose Verwaltung sich gegenseitig ausschließender Steuerelemente verbessert. Erfahren Sie mehr!
type: docs
weight: 60
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

Ruft eine Zeichenfolge ab oder legt sie fest, die eine Gruppe sich gegenseitig ausschließender Steuerelemente angibt. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string GroupName { get; set; }
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
