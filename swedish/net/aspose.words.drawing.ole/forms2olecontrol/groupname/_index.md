---
title: Forms2OleControl.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen Forms2OleControl GroupName förbättrar användarupplevelsen genom att hantera ömsesidigt uteslutande kontroller utan problem. Läs mer!
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

Hämtar eller anger en sträng som anger en grupp av ömsesidigt uteslutande kontroller. Standardvärdet är en tom sträng.

```csharp
public string GroupName { get; set; }
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

* class [Forms2OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
