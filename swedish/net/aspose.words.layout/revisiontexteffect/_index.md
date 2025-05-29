---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Layout.RevisionTextEffect-enum för att förbättra dokumentrevisioner med unika textdekorationseffekter. Förbättra din redigeringsupplevelse!
type: docs
weight: 3850
url: /sv/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Gör det möjligt att ange dekorationseffekt för revideringar av dokumenttext.

```csharp
public enum RevisionTextEffect
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inga specialeffekter har tillämpats på reviderat innehåll. Detta motsvararNoHighlight . |
| Color | `1` | Reviderat innehåll är endast markerat med färg. |
| Bold | `2` | Reviderat innehåll är fetstilt och färglagt. |
| Italic | `3` | Reviderat innehåll är kursiverat och färglagt. |
| Underline | `4` | Reviderat innehåll är understruket och färglagt. |
| DoubleUnderline | `5` | Reviderat innehåll är dubbelt understruket och färglagt. |
| StrikeThrough | `6` | Reviderat innehåll är genomstrykt och färglagt. |
| DoubleStrikeThrough | `7` | Reviderat innehåll är dubbelt genomstruket och färglagt. |
| Hidden | `8` | Reviderat innehåll är dolt. |

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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
