---
title: OleControl.IsForms2OleControl
second_title: Aspose.Words för .NET API Referens
description: OleControl fast egendom. Returnerar sant om kontrollen är enForms2OleControl .
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/olecontrol/isforms2olecontrol/
---
## OleControl.IsForms2OleControl property

Returnerar sant om kontrollen är en[`Forms2OleControl`](../../forms2olecontrol/) .

```csharp
public virtual bool IsForms2OleControl { get; }
```

### Exempel

Visar hur du verifierar egenskaperna för en ActiveX-kontroll.

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

### Se även

* class [OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../olecontrol/)
* hopsättning [Aspose.Words](../../../)


