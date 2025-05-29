---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.OleControl för att sömlöst integrera OLE ActiveX-kontroller i dina applikationer för förbättrad funktionalitet.
type: docs
weight: 1500
url: /sv/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

Representerar OLE ActiveX-kontroll.

För att lära dig mer, besök[Arbeta med Ole-objekt](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public class OleControl
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returer`sann` om kontrollen är en[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Hämtar eller anger namnet på ActiveX-kontrollen. |

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

* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
