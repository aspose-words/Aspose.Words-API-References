---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.CheckBoxControl för att enkelt växla mellan kryssrutors värden och förbättra din dokumentautomation med sömlös integration.
type: docs
weight: 1440
url: /sv/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

Kryssrutekontrollen växlar mellan ett värde.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Hämtar eller anger en bakgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Hämtar eller anger en Caption-egenskap för kontrollen. Standardvärdet är en tom sträng. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar antingen detta`CheckBoxControl` är markerad eller inte. Standardvärdet är`falsk` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Hämtar en samling omedelbara underkontroller. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returer`sann` om kontrollen är i aktiverat tillstånd. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Hämtar eller ställer in en förgrundsfärg för kontrollen. Standardvärdet beror på kontrollens typ. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Hämtar eller anger en sträng som anger en grupp av ömsesidigt uteslutande kontroller. Standardvärdet är en tom sträng. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Hämtar eller ställer in en höjd på kontrollen i punkter. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returer`sann` om kontrollen är en[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Hämtar eller anger namnet på ActiveX-kontrollen. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Hämtar typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Hämtar underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har en markerad alternativknapp värdet '1' medan en omarkerad har värdet '0'. Standardvärdet är en tom sträng. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Hämtar eller ställer in en bredd på kontrollen i punkter. |

## Anmärkningar

Den har tre möjliga tillstånd: vald, avmarkerad och varken vald eller avmarkerad, vilket betyder en kombination av på- och av-tillstånd.

## Exempel

Visar hur man ändrar status för CheckBox-kontrollen.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Se även

* class [MorphDataControl](../morphdatacontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
