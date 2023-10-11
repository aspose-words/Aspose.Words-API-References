---
title: Class Forms2OleControl
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Ole.Forms2OleControl klass. Representerar Microsoft Forms 2.0 OLEkontroll.
type: docs
weight: 1110
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Representerar Microsoft Forms 2.0 OLE-kontroll.

För att lära dig mer, besök[Arbeta med Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Får Caption-egenskapen för kontroll. Standardvärdet är en tom sträng. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Får en samling av omedelbara barnkontroller. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Returnerar`Sann` om kontrollen är i aktiverat tillstånd. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Hämtar eller ställer in en sträng som anger en grupp av ömsesidigt uteslutande kontroller. Standardvärdet är en tom sträng. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Returnerar`Sann` om kontrollen är en`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Hämtar eller ställer in namnet på ActiveX-kontrollen. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Får typ av Forms 2.0-kontroll. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Får underliggande värdeegenskap som ofta representerar kontrolltillstånd. Till exempel har markerad alternativknapp '1'-värde medan omarkerad har '0'. Standardvärdet är en tom sträng. |

### Exempel

Visar hur du verifierar egenskaperna för en ActiveX-kontroll.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Observera att du inte kan ställa in GroupName för en ram.
    checkBox.GroupName = "Aspose group name";
}
```

### Se även

* class [OleControl](../olecontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)


