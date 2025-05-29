---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Layout.RevisionTextEffect, um Dokumentrevisionen mit einzigartigen Textdekorationseffekten zu verbessern. Verbessern Sie Ihr Bearbeitungserlebnis!
type: docs
weight: 3850
url: /de/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Ermöglicht die Angabe von Dekorationseffekten für Überarbeitungen des Dokumenttextes.

```csharp
public enum RevisionTextEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Überarbeiteter Inhalt hat keine Spezialeffekte angewendet. Dies entsprichtNoHighlight . |
| Color | `1` | Überarbeitete Inhalte werden nur farblich hervorgehoben. |
| Bold | `2` | Überarbeitete Inhalte werden fett und farbig dargestellt. |
| Italic | `3` | Überarbeitete Inhalte werden kursiv und farbig dargestellt. |
| Underline | `4` | Überarbeitete Inhalte sind unterstrichen und farblich hervorgehoben. |
| DoubleUnderline | `5` | Überarbeiteter Inhalt ist doppelt unterstrichen und farblich hervorgehoben. |
| StrikeThrough | `6` | Überarbeitete Inhalte sind durchgestrichen und farbig dargestellt. |
| DoubleStrikeThrough | `7` | Überarbeiteter Inhalt ist doppelt durchgestrichen und farbig. |
| Hidden | `8` | Überarbeiteter Inhalt ist ausgeblendet. |

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
