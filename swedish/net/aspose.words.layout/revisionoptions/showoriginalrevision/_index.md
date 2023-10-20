---
title: RevisionOptions.ShowOriginalRevision
linktitle: ShowOriginalRevision
articleTitle: ShowOriginalRevision
second_title: Aspose.Words för .NET
description: RevisionOptions ShowOriginalRevision fast egendom. Tillåter att ange om den ursprungliga texten ska visas istället för en reviderad. Standardvärdet ärfalsk  i C#.
type: docs
weight: 170
url: /sv/net/aspose.words.layout/revisionoptions/showoriginalrevision/
---
## RevisionOptions.ShowOriginalRevision property

Tillåter att ange om den ursprungliga texten ska visas istället för en reviderad. Standardvärdet är`falsk` .

```csharp
public bool ShowOriginalRevision { get; set; }
```

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

* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
