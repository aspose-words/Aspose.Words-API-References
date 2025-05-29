---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OleControl Name för att enkelt hantera namnet på din ActiveX-kontroll. Förbättra funktionaliteten och effektivisera din utvecklingsprocess idag!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Hämtar eller anger namnet på ActiveX-kontrollen.

```csharp
public string Name { get; set; }
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

* class [OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
