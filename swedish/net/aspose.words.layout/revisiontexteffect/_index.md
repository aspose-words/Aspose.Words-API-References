---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words för .NET
description: Aspose.Words.Layout.RevisionTextEffect uppräkning. Tillåter att specificera dekorationseffekt för revisioner av dokumenttext i C#.
type: docs
weight: 3400
url: /sv/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Tillåter att specificera dekorationseffekt för revisioner av dokumenttext.

```csharp
public enum RevisionTextEffect
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Reviderat innehåll har inga specialeffekter tillämpade. Detta motsvararNoHighlight . |
| Color | `1` | Reviderat innehåll markeras endast med färg. |
| Bold | `2` | Reviderat innehåll görs fet och färgad. |
| Italic | `3` | Reviderat innehåll är kursivt och färglagt. |
| Underline | `4` | Reviderat innehåll är understruket och färglagt. |
| DoubleUnderline | `5` | Reviderat innehåll är dubbelt understruket och färgat. |
| StrikeThrough | `6` | Reviderat innehåll stryks igenom och färgläggs. |
| DoubleStrikeThrough | `7` | Reviderat innehåll är dubbelstruket och färglagt. |
| Hidden | `8` | Reviderat innehåll är dolt. |

## Exempel

Visar hur man ändrar utseendet på revisioner.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Hämta RevisionOptions-objektet som styr utseendet på revisioner.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Gör insättningsrevisioner i grönt och kursivt.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Gör raderingsrevisioner i rött och fetstil.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Samma text kommer att visas två gånger i en rörelserevision:
// en gång vid avgångsplatsen och en gång vid ankomstdestinationen.
// Gör texten vid den flyttade från revisionen gul med dubbel genomstrykning
// och dubbelt understruket blått vid den flyttade till revisionen.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Gör formatrevisioner i mörkrött och fetstil.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Placera en tjock mörkblå stapel till vänster på sidan bredvid rader som påverkas av ändringar.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Visa revisionsmärken och originaltext.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Få rörelse, radering, formateringsrevisioner och kommentarer att dyka upp i gröna ballonger
// till höger på sidan.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Dessa funktioner är endast tillämpliga på format som .pdf eller .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
