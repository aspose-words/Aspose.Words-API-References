---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OleFormat SuggestedFileName för att enkelt hämta det rekommenderade filnamnet för att spara dina inbäddade objekt sömlöst.
type: docs
weight: 130
url: /sv/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Hämtar det föreslagna filnamnet för det aktuella inbäddade objektet om du vill spara det i en fil.

```csharp
public string SuggestedFileName { get; }
```

## Exempel

Visar hur man hämtar ett OLE-objekts föreslagna filnamn.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE-objekt kan ge ett förslag på filnamn och filändelse,
// som vi kan använda när vi sparar objektets innehåll till en fil i det lokala filsystemet.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Se även

* class [OleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
