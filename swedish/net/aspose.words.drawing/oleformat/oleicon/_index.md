---
title: OleFormat.OleIcon
second_title: Aspose.Words för .NET API Referens
description: OleFormat fast egendom. Hämtar ritaspekten för OLEobjektet. När Sann  visas OLEobjektet som en ikon. När falsk  visas OLEobjektet som innehåll.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Hämtar ritaspekten för OLE-objektet. När **Sann** , visas OLE-objektet som en ikon. När **falsk** , visas OLE-objektet som innehåll.

```csharp
public bool OleIcon { get; }
```

### Anmärkningar

Aspose.Words tillåter inte att ställa in den här egenskapen för att undvika förvirring. Om du kunde ändra ritaspekten i Aspose.Words, skulle Microsoft Word fortfarande visa OLE-objektet i dess ursprungliga ritaspekt tills du redigerar eller uppdaterar OLE-objektet i Microsoft Word.

### Exempel

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

// Om objektet innehåller OLE-data kan vi komma åt det med en ström.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


