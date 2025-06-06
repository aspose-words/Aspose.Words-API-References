---
title: OleFormat.AutoUpdate
linktitle: AutoUpdate
articleTitle: AutoUpdate
second_title: Aspose.Words för .NET
description: Upptäck OleFormat AutoUpdate-egenskapen i Microsoft Word, som säkerställer att dina OLE-objektlänkar hålls aktuella och förbättrar dokumentets noggrannhet utan problem.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/oleformat/autoupdate/
---
## OleFormat.AutoUpdate property

Anger om länken till OLE-objektet uppdateras automatiskt eller inte i Microsoft Word.

```csharp
public bool AutoUpdate { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

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
