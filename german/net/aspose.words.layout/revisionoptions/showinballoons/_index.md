---
title: RevisionOptions.ShowInBalloons
second_title: Aspose.Words für .NET-API-Referenz
description: RevisionOptions eigendom. Ermöglicht die Angabe ob die Revisionen in den Sprechblasen gerendert werden. Der Standardwert istNone .
type: docs
weight: 160
url: /de/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Ermöglicht die Angabe, ob die Revisionen in den Sprechblasen gerendert werden. Der Standardwert istNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### Bemerkungen

Beachten Sie, dass Überarbeitungen nicht in Sprechblasen für gerendert werdenShowInAnnotations .

### Beispiele

Zeigt, wie Revisionen in Sprechblasen angezeigt werden.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Standardmäßig hat Text, der eine Revision ist, eine andere Farbe, um ihn von anderem Nicht-Revisionstext zu unterscheiden.
// Legen Sie eine Überarbeitungsoption fest, um weitere Details zu jeder Überarbeitung in einer Sprechblase am rechten Rand der Seite anzuzeigen.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../revisionoptions/)
* Montage [Aspose.Words](../../../)


