---
title: Forms2OleControl.Value
second_title: Aspose.Words för .NET API Referens
description: Forms2OleControl fast egendom. Får underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har markerad alternativknapp 1värde medan omarkerad har 0. Standardvärdet är en tom sträng.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Får underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har markerad alternativknapp '1'-värde medan omarkerad har '0'. Standardvärdet är en tom sträng.

```csharp
public string Value { get; }
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

* class [Forms2OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* hopsättning [Aspose.Words](../../../)


