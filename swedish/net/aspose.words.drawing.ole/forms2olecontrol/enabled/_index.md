---
title: Forms2OleControl.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words för .NET
description: Forms2OleControl Enabled fast egendom. ReturnerarSann om kontrollen är i aktiverat tillstånd i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Returnerar`Sann` om kontrollen är i aktiverat tillstånd.

```csharp
public bool Enabled { get; }
```

## Exempel

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

* class [Forms2OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
