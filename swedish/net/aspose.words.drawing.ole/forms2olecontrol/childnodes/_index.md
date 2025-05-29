---
title: Forms2OleControl.ChildNodes
linktitle: ChildNodes
articleTitle: ChildNodes
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Forms2OleControl ChildNodes för att enkelt komma åt och hantera omedelbara underordnade kontroller för förbättrad funktionalitet.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Hämtar en samling omedelbara underkontroller.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

## Anmärkningar

Returer`null` om den här kontrollen inte kan ha underordnade.

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

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
