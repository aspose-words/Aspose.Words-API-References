---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.TextBoxControl för att enkelt visa organiserad text från data eller användarinmatning. Förbättra din dokumenthantering idag!
type: docs
weight: 1520
url: /sv/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

TextBox-kontrollen visar text från en organiserad datamängd eller användarinmatning.

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Hämtar eller anger en text från kontrollen. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Hämtar typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Hämtar underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har en markerad alternativknapp värdet '1' medan en omarkerad har värdet '0'. Standardvärdet är en tom sträng. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Hämtar eller ställer in en bredd på kontrollen i punkter. |

## Exempel

Visar hur man ändrar texten i TextBox OLE-kontrollen.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Se även

* class [MorphDataControl](../morphdatacontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
