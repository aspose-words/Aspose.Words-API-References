---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RevisionOptions ShowInBalloons! Kontrollera revisionssynligheten i ballonger för förbättrad dokumenttydlighet. Standardinställningen är Ingen.
type: docs
weight: 180
url: /sv/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Gör det möjligt att ange om revisionerna ska renderas i ballongerna. Standardvärdet ärNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Anmärkningar

Observera att revisioner inte återges i ballonger förShowInAnnotations .

## Exempel

Visar hur man visar revisioner i ballonger.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Som standard har text som är en revision en annan färg för att skilja den från annan text som inte är revision.
// Ange ett revisionsalternativ för att visa mer information om varje revision i en ballong i sidans högra marginal.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
