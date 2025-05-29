---
title: RevisionOptions.RevisionBarsWidth
linktitle: RevisionBarsWidth
articleTitle: RevisionBarsWidth
second_title: Aspose.Words för .NET
description: Hantera ditt dokuments revisionsstaplar med egenskapen RevisionBarsWidth i RevisionOptions. Anpassa enkelt bredden för tydlig synlighet och organisation.
type: docs
weight: 170
url: /sv/net/aspose.words.layout/revisionoptions/revisionbarswidth/
---
## RevisionOptions.RevisionBarsWidth property

Hämtar eller ställer in bredden på revisionsstaplar och punkter.

```csharp
public float RevisionBarsWidth { get; set; }
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
