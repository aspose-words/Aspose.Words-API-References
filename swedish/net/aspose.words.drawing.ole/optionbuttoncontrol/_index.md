---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.OptionButtonControl, perfekt för att skapa exklusiva valmöjligheter i dina applikationer. Förbättra användarupplevelsen idag!
type: docs
weight: 1510
url: /sv/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

Alternativknappskontrollen möjliggör ett enda val i en begränsad uppsättning ömsesidigt uteslutande val.

```csharp
public class OptionButtonControl : MorphDataControl
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Hämtar eller anger en bakgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Hämtar eller anger en Caption-egenskap för kontrollen. Standardvärdet är en tom sträng. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Hämtar en samling omedelbara underkontroller. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returer`sann` om kontrollen är i aktiverat tillstånd. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Hämtar eller ställer in en förgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Hämtar eller anger en sträng som anger en grupp av ömsesidigt uteslutande kontroller. Standardvärdet är en tom sträng. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Hämtar eller ställer in en höjd på kontrollen i punkter. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returer`sann` om kontrollen är en[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Hämtar eller anger namnet på ActiveX-kontrollen. |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar antingen detta`OptionButtonControl` är vald eller inte. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Hämtar typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Hämtar underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har en markerad alternativknapp värdet '1' medan en omarkerad har värdet '0'. Standardvärdet är en tom sträng. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Hämtar eller ställer in en bredd på kontrollen i punkter. |

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

* class [MorphDataControl](../morphdatacontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
