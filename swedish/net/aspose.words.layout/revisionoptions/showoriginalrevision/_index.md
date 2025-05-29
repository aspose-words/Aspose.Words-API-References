---
title: RevisionOptions.ShowOriginalRevision
linktitle: ShowOriginalRevision
articleTitle: ShowOriginalRevision
second_title: Aspose.Words för .NET
description: Kontrollera dina dokumentrevisioner med egenskapen ShowOriginalRevision. Växla enkelt mellan original- och reviderad text för tydligare insikter. Standardinställningen är falsk.
type: docs
weight: 190
url: /sv/net/aspose.words.layout/revisionoptions/showoriginalrevision/
---
## RevisionOptions.ShowOriginalRevision property

Gör det möjligt att ange om originaltexten ska visas istället för den reviderade. Standardvärdet är`falsk` .

```csharp
public bool ShowOriginalRevision { get; set; }
```

## Exempel

Visar hur man ändrar utseendet på revisioner.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Hämta RevisionOptions-objektet som styr utseendet på revisioner.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Rendera infogningsrevideringar i grönt och kursiv stil.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Rendera borttagna revisioner i rött och fetstil.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Samma text kommer att förekomma två gånger i en satsrevision:
// en gång vid avgångspunkten och en gång vid ankomstdestinationen.
// Gör texten vid den flyttade versionen gul med en dubbel överstrykning
// och dubbelt understruken blå vid den flyttade versionen.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Rendera formatrevideringar i mörkrött och fetstil.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Placera en tjock mörkblå stapel på vänster sida av sidan bredvid rader som påverkas av revisioner.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Visa revisionsmarkeringar och originaltext.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Få flyttningar, borttagningar, formateringsändringar och kommentarer att visas i gröna ballonger
// på höger sida av sidan.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Dessa funktioner gäller endast för format som .pdf eller .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Se även

* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
