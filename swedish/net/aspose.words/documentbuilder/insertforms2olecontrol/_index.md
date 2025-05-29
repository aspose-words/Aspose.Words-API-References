---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words för .NET
description: Integrera Forms2OleControl enkelt med DocumentBuilders InsertForms2OleControl-metod. Förbättra din dokumentfunktionalitet idag!
type: docs
weight: 350
url: /sv/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Insatser[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) objekt till aktuell position.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Returvärde

[`Shape`](../../../aspose.words.drawing/shape/) objekt som innehåller godkänt[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Exempel

Visar hur man infogar ActiveX-kontroll.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Se även

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
