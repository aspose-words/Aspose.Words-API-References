---
title: Forms2OleControl.Caption
linktitle: Caption
articleTitle: Caption
second_title: Aspose.Words für .NET
description: Entdecken Sie die Caption-Eigenschaft von Forms2OleControl, um den Titel Ihres Steuerelements einfach anzupassen. Verbessern Sie die Benutzerfreundlichkeit mit dieser einfachen und effektiven Funktion.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Ruft eine Caption-Eigenschaft des Steuerelements ab oder legt diese fest. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string Caption { get; set; }
```

## Beispiele

Zeigt, wie die Beschriftung für das ActiveX-Steuerelement festgelegt wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl() { Caption = "Button caption" };
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual("Button caption", button1.Caption);
```

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
