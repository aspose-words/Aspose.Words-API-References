---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.RevisionTextEffect opsomming. Ermöglicht die Festlegung eines Dekorationseffekts für Überarbeitungen des Dokumenttexts in C#.
type: docs
weight: 3400
url: /de/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Ermöglicht die Festlegung eines Dekorationseffekts für Überarbeitungen des Dokumenttexts.

```csharp
public enum RevisionTextEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Auf den überarbeiteten Inhalt wurden keine Spezialeffekte angewendet. Dies entsprichtNoHighlight . |
| Color | `1` | Überarbeiteter Inhalt wird nur farblich hervorgehoben. |
| Bold | `2` | Überarbeiteter Inhalt wird fett und farbig dargestellt. |
| Italic | `3` | Überarbeiteter Inhalt wird kursiv und farbig dargestellt. |
| Underline | `4` | Überarbeiteter Inhalt ist unterstrichen und farbig. |
| DoubleUnderline | `5` | Überarbeiteter Inhalt ist doppelt unterstrichen und farbig. |
| StrikeThrough | `6` | Überarbeiteter Inhalt wird durchgestrichen und eingefärbt. |
| DoubleStrikeThrough | `7` | Überarbeiteter Inhalt ist doppelt durchgestrichen und eingefärbt. |
| Hidden | `8` | Überarbeiteter Inhalt ist ausgeblendet. |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
