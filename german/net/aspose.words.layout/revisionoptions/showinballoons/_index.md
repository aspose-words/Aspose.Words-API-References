---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ShowInBalloons“ von RevisionOptions! Steuern Sie die Sichtbarkeit von Revisionen in Sprechblasen für eine bessere Dokumentübersicht. Standardmäßig ist „Keine“ eingestellt.
type: docs
weight: 180
url: /de/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Ermöglicht die Angabe, ob die Revisionen in den Sprechblasen dargestellt werden. Der Standardwert istNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Bemerkungen

Beachten Sie, dass Revisionen nicht in Sprechblasen dargestellt werden fürShowInAnnotations .

## Beispiele

Zeigt, wie Revisionen in Sprechblasen angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Standardmäßig hat Text, der eine Revision darstellt, eine andere Farbe, um ihn von dem übrigen Text, der keine Revision darstellt, zu unterscheiden.
// Legen Sie eine Revisionsoption fest, um in einer Sprechblase am rechten Rand der Seite weitere Details zu jeder Revision anzuzeigen.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

Zeigt, wie das Erscheinungsbild von Revisionen geändert wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Holen Sie sich das RevisionOptions-Objekt, das das Erscheinungsbild von Revisionen steuert.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Rendern Sie Einfügungsrevisionen in Grün und Kursivschrift.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Löschrevisionen in Rot und Fettdruck darstellen.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Derselbe Text erscheint zweimal in einer Bewegungsrevision:
// einmal am Abfahrtsort und einmal am Zielort.
// Den Text in der verschobenen Revision gelb und doppelt durchgestrichen darstellen
// und doppelt blau unterstrichen bei der verschobenen Revision.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Formatrevisionen in Dunkelrot und Fettdruck rendern.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Platzieren Sie einen dicken dunkelblauen Balken auf der linken Seite der Seite neben den von Revisionen betroffenen Zeilen.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Revisionsmarkierungen und Originaltext anzeigen.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Bewegung, Löschung, Formatierungsänderungen und Kommentare werden in grünen Sprechblasen angezeigt
// auf der rechten Seite der Seite.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Diese Funktionen sind nur auf Formate wie .pdf oder .jpg anwendbar.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Siehe auch

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
