---
title: OleFormat.SuggestedExtension
linktitle: SuggestedExtension
articleTitle: SuggestedExtension
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OleFormat SuggestedExtension för att enkelt få den perfekta filändelsen för att effektivt spara dina inbäddade objekt.
type: docs
weight: 120
url: /sv/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Hämtar den föreslagna filändelsen för det aktuella inbäddade objektet om du vill spara det i en fil.

```csharp
public string SuggestedExtension { get; }
```

## Exempel

Visar hur man extraherar inbäddade OLE-objekt till filer.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// OLE-objektet i den första formen är ett Microsoft Excel-kalkylblad.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Vårt mål är varken automatisk uppdatering eller låst från uppdateringar.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Om vi planerar att spara OLE-objektet till en fil i det lokala filsystemet,
// vi kan använda egenskapen "SuggestedExtension" för att avgöra vilket filtillägg som ska tillämpas på filen.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Nedan följer två sätt att spara ett OLE-objekt till en fil i det lokala filsystemet.
// 1 - Spara det via en ström:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Spara det direkt till ett filnamn:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
