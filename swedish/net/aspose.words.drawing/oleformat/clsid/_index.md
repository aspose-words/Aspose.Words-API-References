---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words för .NET
description: Upptäck OleFormat Clsid-egenskapen för att enkelt hämta CLSID för OLE-objekt, vilket förbättrar programmets funktionalitet och prestanda.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Hämtar CLSID för OLE-objektet.

```csharp
public Guid Clsid { get; }
```

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

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
