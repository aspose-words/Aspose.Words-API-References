---
title: Forms2OleControl.ChildNodes
second_title: Aspose.Words für .NET-API-Referenz
description: Forms2OleControl eigendom. Ruft Sammlung von unmittelbar untergeordneten Steuerelementen ab.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Ruft Sammlung von unmittelbar untergeordneten Steuerelementen ab.

```csharp
public Forms2OleControlCollection ChildNodes { get; }
```

### Bemerkungen

Kehrt zurück **Null** wenn diese Kontrolle keine Kinder haben kann.

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

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* Montage [Aspose.Words](../../../)


