---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CommandButtonControl Type för att enkelt komma åt kontrolltyper i Forms 2.0, vilket förbättrar programmets funktionalitet och användarupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Hämtar typ av Forms 2.0-kontroll.

```csharp
public override Forms2OleControlType Type { get; }
```

## Exempel

Visar hur man infogar ActiveX-kontroll.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Se även

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
