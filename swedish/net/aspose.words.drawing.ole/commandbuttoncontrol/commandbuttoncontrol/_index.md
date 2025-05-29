---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words för .NET
description: Upptäck CommandButtonControl-konstruktorn. Skapa och anpassa knappar för dina applikationer enkelt med denna kraftfulla klassinstans.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Initierar en ny instans av[`CommandButtonControl`](../) klass.

```csharp
public CommandButtonControl()
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

* class [CommandButtonControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
