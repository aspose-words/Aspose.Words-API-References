---
title: Class FootnoteOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Notes.FootnoteOptions klas. Stellt die Fußnotennummerierungsoptionen für ein Dokument oder einen Abschnitt dar.
type: docs
weight: 4280
url: /de/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Stellt die Fußnotennummerierungsoptionen für ein Dokument oder einen Abschnitt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Fußnote und Endnote](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) Dokumentationsartikel.

```csharp
public sealed class FootnoteOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Gibt die Anzahl der Spalten an, mit denen der Fußnotenbereich formatiert wird. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Gibt das Zahlenformat für automatisch nummerierte Fußnoten an. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Gibt die Position der Fußnoten an. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Legt fest, wann die automatische Nummerierung neu startet. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | Gibt die Startnummer oder das Anfangszeichen für die ersten automatisch nummerierten Fußnoten an. |

### Beispiele

Zeigt, wie der Fußnotenabschnitt in eine bestimmte Anzahl von Spalten aufgeteilt wird.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Fußnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Fußnote ist eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erzeugt auch einen Eintrag am Ende der Seite, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertFootnote“ des Document Builders übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Wir können die Eigenschaft „Position“ verwenden, um zu bestimmen, wo das Dokument alle seine Fußnoten platzieren soll.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BottomOfPage“ setzen,
// Jede Fußnote wird am Ende der Seite angezeigt, die ihre Referenzmarke enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BeneathText“ setzen,
// Jede Fußnote wird am Ende des Seitentextes angezeigt, der ihre Referenzmarke enthält.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Zeigt, wie man eine Zahl festlegt, bei der das Dokument mit der Fußnoten-/Endnotenzählung beginnt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote/Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt auch einen Eintrag, der aus einem Symbol besteht
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die „InsertEndnote“-Methode des Document Builders übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die Folgendes enthält
// Ihre Referenzsymbole und Endnoten werden am Ende des Dokuments angezeigt.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten, die beide bei 1 beginnen.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Wir können die Eigenschaft „StartNumber“ verwenden, um das Dokument abzurufen
// Beginnen Sie eine Fußnoten- oder Endnotenzählung mit einer anderen Zahl.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Zeigt, wie der Nummernstil von Fußnoten-/Endnoten-Referenzzeichen geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote/Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt auch einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Document Builders übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die Folgendes enthält
// Ihre Referenzsymbole und Endnoten werden am Ende des Dokuments angezeigt.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten. Standardmäßig werden in Fußnoten ihre Nummern mit arabischen Ziffern angezeigt.
// und Endnoten zeigen ihre Nummern in kleinen römischen Ziffern an.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Wir können die Eigenschaft „NumberStyle“ verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Dies hat keine Auswirkungen auf Fußnoten/Endnoten mit benutzerdefinierten Referenzmarken.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Zeigt, wie die Fußnoten-/Endnotennummerierung an bestimmten Stellen im Dokument neu gestartet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Fußnote/Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt auch einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Document Builders übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die Folgendes enthält
// Ihre Referenzsymbole und Endnoten werden am Ende des Dokuments angezeigt.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und Endnoten und startet diese Zählungen zu keinem Zeitpunkt neu.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Wir können die Eigenschaft „RestartRule“ verwenden, um das Dokument neu zu starten
// die Fußnote/Endnote zählt auf einer neuen Seite oder einem neuen Abschnitt.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Siehe auch

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)


