---
title: RevisionOptions.MovedToTextEffect
linktitle: MovedToTextEffect
articleTitle: MovedToTextEffect
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „MovedToTextEffect“ von RevisionOptions, mit der Sie Texteffekte für verschobene Inhalte anpassen können. Verbessern Sie die Übersichtlichkeit mit dem Standardstil „DoubleUnderline“!
type: docs
weight: 120
url: /de/net/aspose.words.layout/revisionoptions/movedtotexteffect/
---
## RevisionOptions.MovedToTextEffect property

Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet werden soll, in die Inhalte verschoben wurdenMoving . Der Standardwert istDoubleUnderline

```csharp
public RevisionTextEffect MovedToTextEffect { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Werte vonHidden UndDoubleStrikeThrough sind nicht zulässig. |

## Beispiele

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

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
