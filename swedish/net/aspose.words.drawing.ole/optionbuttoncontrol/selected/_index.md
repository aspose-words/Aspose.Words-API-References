---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words för .NET
description: Hantera din OptionButtonControl enkelt! Ställ in eller hämta dess valda tillstånd med ett enkelt booleskt värde för sömlös användarinteraktion.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Hämtar eller ställer in ett booleskt värde som indikerar antingen detta[`OptionButtonControl`](../) är vald eller inte.

```csharp
public bool Selected { get; set; }
```

## Anmärkningar

Observera att den här egenskapen låter dig välja flera objekt i en grupp av[`OptionButtonControl`](../) med samma[`GroupName`](../../forms2olecontrol/groupname/) Det är upp till dig att avmarkera ett tidigare valt objekt när du gör detta[`OptionButtonControl`](../) vald.

## Exempel

Visar hur man väljer radioknapp.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Avmarkera valt första objekt.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Välj den andra alternativknappen.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Se även

* class [OptionButtonControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
