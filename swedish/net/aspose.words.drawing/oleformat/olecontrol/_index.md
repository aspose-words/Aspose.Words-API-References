---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words för .NET
description: Upptäck OleFormat OleControl-egenskapen för att komma åt ActiveX-kontrollobjekt. Lås upp förbättrad funktionalitet och integration för dina OLE-applikationer.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Får`OleControl` objekt om detta OLE-objekt är en ActiveX-kontroll. Annars är egenskapen null.

```csharp
public OleControl OleControl { get; }
```

## Exempel

Visar hur man verifierar egenskaperna för en ActiveX-kontroll.

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

    // Observera att du inte kan ange gruppnamn för en ram.
    checkBox.GroupName = "Aspose group name";
}
```

### Se även

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
