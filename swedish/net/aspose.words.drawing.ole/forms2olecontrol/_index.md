---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.Forms2OleControl, din lösning för att integrera Microsoft Forms 2.0 OLE-kontroller sömlöst i dina applikationer.
type: docs
weight: 1460
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Representerar Microsoft Forms 2.0 OLE-kontroll.

För att lära dig mer, besök[Arbeta med Ole-objekt](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public abstract class Forms2OleControl : OleControl
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
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returer`sann` om kontrollen är en`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Hämtar eller anger namnet på ActiveX-kontrollen. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Hämtar typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Hämtar underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har en markerad alternativknapp värdet '1' medan en omarkerad har värdet '0'. Standardvärdet är en tom sträng. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Hämtar eller ställer in en bredd på kontrollen i punkter. |

## Exempel

Visar hur man verifierar egenskaperna för en ActiveX-kontroll.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Observera att du inte kan ange gruppnamn för en ram.
    checkBox.GroupName = "Aspose group name";
}
```

### Se även

* class [OleControl](../olecontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
