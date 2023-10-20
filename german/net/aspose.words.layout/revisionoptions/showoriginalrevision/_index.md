---
title: RevisionOptions.ShowOriginalRevision
linktitle: ShowOriginalRevision
articleTitle: ShowOriginalRevision
second_title: Aspose.Words für .NET
description: RevisionOptions ShowOriginalRevision eigendom. Ermöglicht die Angabe ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert istFALSCH  in C#.
type: docs
weight: 170
url: /de/net/aspose.words.layout/revisionoptions/showoriginalrevision/
---
## RevisionOptions.ShowOriginalRevision property

Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowOriginalRevision { get; set; }
```

## Beispiele

Zeigt, wie das Erscheinungsbild von Revisionen geändert wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Holen Sie sich das RevisionOptions-Objekt, das die Darstellung von Revisionen steuert.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Einfügungsrevisionen in Grün und Kursiv darstellen.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Löschrevisionen rot und fett darstellen.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Derselbe Text erscheint zweimal in einer Bewegungsrevision:
// einmal am Abfahrtsort und einmal am Ankunftsort.
// Rendern Sie den Text in der Revision, aus der er verschoben wurde, gelb und doppelt durchgestrichen
// und doppelt unterstrichen blau bei der verschobenen Revision.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Formatrevisionen dunkelrot und fett darstellen.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Platzieren Sie einen dicken dunkelblauen Balken auf der linken Seite der Seite neben den von Revisionen betroffenen Zeilen.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Revisionsmarkierungen und Originaltext anzeigen.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Bewegungen, Löschungen, Formatierungsänderungen und Kommentare werden in grünen Sprechblasen angezeigt
// auf der rechten Seite der Seite.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Diese Funktionen gelten nur für Formate wie .pdf oder .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Siehe auch

* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
