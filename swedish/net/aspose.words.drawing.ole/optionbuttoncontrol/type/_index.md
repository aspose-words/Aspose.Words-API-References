---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OptionButtonControl Type för Forms 2.0. Lär dig hur du förbättrar dina formulär med den här viktiga kontrolltypsfunktionen.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Hämtar typ av Forms 2.0-kontroll.

```csharp
public override Forms2OleControlType Type { get; }
```

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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
