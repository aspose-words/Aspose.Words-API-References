---
title: RevisionOptions.RevisionBarsColor
second_title: Aspose.Words für .NET-API-Referenz
description: RevisionOptions eigendom. Ermöglicht die Angabe der Farbe die für Seitenleisten verwendet werden soll die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert istRed .
type: docs
weight: 130
url: /de/net/aspose.words.layout/revisionoptions/revisionbarscolor/
---
## RevisionOptions.RevisionBarsColor property

Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet werden soll, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert istRed .

```csharp
public RevisionColor RevisionBarsColor { get; set; }
```

### Bemerkungen

Setzen Sie diese Eigenschaft aufByAuthor oderNoHighlight values führt dazu, dass Revisionsbalken aus dem Layout ausgeblendet werden.

### Beispiele

Zeigt, wie das Erscheinungsbild von Revisionen geändert wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Abrufen des RevisionOptions-Objekts, das die Darstellung von Revisionen steuert.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Einfügungsrevisionen in grün und kursiv darstellen.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Löschrevisionen rot und fett darstellen.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Derselbe Text erscheint zweimal in einer Bewegungsrevision:
// einmal am Abfahrtsort und einmal am Zielort.
// Rendern Sie den Text an der verschobenen Revision gelb mit einem doppelten Durchstrich
// und doppelt unterstrichen blau bei der verschobenen Revision.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Überarbeitungen des Formats in dunkelrot und fett darstellen.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Platzieren Sie einen dicken dunkelblauen Balken auf der linken Seite der Seite neben Zeilen, die von Überarbeitungen betroffen sind.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Überarbeitungsmarkierungen und Originaltext anzeigen.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Erhalten Sie Verschiebungen, Löschungen, Formatierungsüberarbeitungen und Kommentare, die in grünen Sprechblasen angezeigt werden
// auf der rechten Seite der Seite.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Diese Funktionen gelten nur für Formate wie .pdf oder .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Siehe auch

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../revisionoptions/)
* Montage [Aspose.Words](../../../)


