---
title: Class Forms2OleControlCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Ole.Forms2OleControlCollection klass. Representerar samling avForms2OleControl objekt.
type: docs
weight: 990
url: /sv/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Representerar samling av[`Forms2OleControl`](../forms2olecontrol/) objekt.

```csharp
public class Forms2OleControlCollection
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Får antalet objekt i samlingen. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Blir[`Forms2OleControl`](../forms2olecontrol/)objekt vid angivet index. |

### Exempel

Visar hur man kommer åt en OLE-kontroll inbäddad i ett dokument och dess underordnade kontroller.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Former lagrar och visar OLE-objekt i dokumentets kropp.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Vissa OLE-kontroller kan innehålla underordnade kontroller, till exempel den i detta dokument med tre alternativknappar.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)


