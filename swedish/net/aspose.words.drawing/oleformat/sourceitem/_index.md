---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: Aspose.Words för .NET
description: Upptäck OleFormat SourceItem-egenskapen och identifiera och hantera enkelt länkade delar av din källfil med denna viktiga strängfunktion.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

Hämtar eller anger en sträng som används för att identifiera den del av källfilen som länkas.

```csharp
public string SourceItem { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Om källfilen till exempel är en Microsoft Excel-arbetsbok,`SourceItem` Egenskapen kan returnera "Workbook1!R3C1:R4C2" om OLE-objektet bara innehåller ett fåtal celler från kalkylbladet.

## Exempel

Visar hur man infogar länkade och olänkade OLE-objekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bädda in en Microsoft Visio-ritning i dokumentet som ett OLE-objekt.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Infoga en länk till filen i det lokala filsystemet och visa den som en ikon.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// Genom att infoga OLE-objekt skapas former som lagrar dessa objekt.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Om en form innehåller ett OLE-objekt kommer den att ha en giltig "OleFormat"-egenskap,
// som vi kan använda för att verifiera vissa aspekter av formen.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Om objektet innehåller OLE-data kan vi komma åt det med hjälp av en ström.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
