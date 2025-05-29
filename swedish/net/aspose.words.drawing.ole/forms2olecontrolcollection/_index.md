---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Ole.Forms2OleControlCollection, din lösning för att effektivt hantera Forms2OleControl-objekt i dokumentbehandling.
type: docs
weight: 1470
url: /sv/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

Representerar en samling av[`Forms2OleControl`](../forms2olecontrol/) objekt.

För att lära dig mer, besök[Arbeta med Ole-objekt](https://docs.aspose.com/words/net/working-with-ole-objects/) dokumentationsartikel.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Hämtar antal objekt i samlingen. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Får[`Forms2OleControl`](../forms2olecontrol/) objekt vid ett angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Hämtar uppräknaren. |

## Exempel

Visar hur man kommer åt en OLE-kontroll som är inbäddad i ett dokument och dess underkontroller.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Former lagrar och visar OLE-objekt i dokumentets brödtext.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Vissa OLE-kontroller kan innehålla underkontroller, till exempel den i det här dokumentet med tre alternativknappar.
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

* class [Forms2OleControl](../forms2olecontrol/)
* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
