---
title: OleFormat.OleControl
second_title: Aspose.Words för .NET API Referens
description: OleFormat fast egendom. BlirOleControl objekt om detta OLEobjekt är en ActiveXkontroll. Annars är den här egenskapen null.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Blir`OleControl` objekt om detta OLE-objekt är en ActiveX-kontroll. Annars är den här egenskapen null.

```csharp
public OleControl OleControl { get; }
```

### Exempel

Visar hur du verifierar egenskaperna för en ActiveX-kontroll.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Observera att du inte kan ställa in GroupName för en ram.
    checkBox.GroupName = "Aspose group name";
}
```

### Se även

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


