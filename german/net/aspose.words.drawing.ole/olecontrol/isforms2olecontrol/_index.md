---
title: OleControl.IsForms2OleControl
second_title: Aspose.Words für .NET-API-Referenz
description: OleControl eigendom. Gibt wahr zurück wenn das Steuerelement a istForms2OleControl .
type: docs
weight: 10
url: /de/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Gibt wahr zurück, wenn das Steuerelement a ist[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public virtual bool IsForms2OleControl { get; }
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


