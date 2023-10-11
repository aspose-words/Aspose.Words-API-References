---
title: OleFormat.IsLocked
second_title: Aspose.Words för .NET API Referens
description: OleFormat fast egendom. Anger om länken till OLEobjektet är låst från uppdateringar.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/oleformat/islocked/
---
## OleFormat.IsLocked property

Anger om länken till OLE-objektet är låst från uppdateringar.

```csharp
public bool IsLocked { get; set; }
```

### Anmärkningar

Standardvärdet är`falsk`.

### Exempel

Visar hur man extraherar inbäddade OLE-objekt till filer.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Vårt objekt är varken automatisk uppdatering eller låst från uppdateringar.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// vi kan använda egenskapen "SuggestedExtension" för att avgöra vilket filtillägg som ska tillämpas på filen.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nedan finns två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 - Spara det via en stream:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Spara det direkt till ett filnamn:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../oleformat/)
* hopsättning [Aspose.Words](../../../)


