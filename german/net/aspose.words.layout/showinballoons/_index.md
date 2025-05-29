---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words.Layout.ShowInBalloons die Dokumentbearbeitung verbessert, indem sie sichtbare Revisionen in Sprechblasen steuert und so eine klare Zusammenarbeit ermöglicht.
type: docs
weight: 3860
url: /de/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Gibt an, welche Revisionen in Sprechblasen gerendert werden.

```csharp
public enum ShowInBalloons
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Rendert das Einfügen, Löschen und Formatieren von Revisionen inline. |
| Format | `1` | Rendert das Einfügen und Löschen von Revisionen inline und formatiert Revisionen in Sprechblasen. |
| FormatAndDelete | `2` | Rendert das Einfügen von Revisionen inline, löscht und formatiert Revisionen in Sprechblasen. |

## Bemerkungen

Beachten Sie, dass Revisionen nicht in Sprechblasen dargestellt werden fürShowInAnnotations .

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
