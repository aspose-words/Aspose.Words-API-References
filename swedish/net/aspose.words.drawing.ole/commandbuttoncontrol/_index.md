---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.CommandButtonControl för att enkelt skapa interaktiva knappar som kör makron, vilket förbättrar användarengagemang i dina applikationer.
type: docs
weight: 1450
url: /sv/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

CommandButton-kontrollen kör ett makro som utför en åtgärd när en användare klickar på det.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Initierar en ny instans av`CommandButtonControl` klass. |

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
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Hämtar typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Hämtar underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har en markerad alternativknapp värdet '1' medan en omarkerad har värdet '0'. Standardvärdet är en tom sträng. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Hämtar eller ställer in en bredd på kontrollen i punkter. |

## Exempel

Visar hur man infogar ActiveX-kontroll.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Se även

* class [Forms2OleControl](../forms2olecontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
