---
title: EndnoteOptions Class
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Notes.EndnoteOptions klas. Stellt die Endnotennummerierungsoptionen für ein Dokument oder einen Abschnitt dar in C#.
type: docs
weight: 4240
url: /de/net/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class

Stellt die Endnotennummerierungsoptionen für ein Dokument oder einen Abschnitt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Fußnote und Endnote](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) Dokumentationsartikel.

```csharp
public sealed class EndnoteOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [NumberStyle](../../aspose.words.notes/endnoteoptions/numberstyle/) { get; set; } | Gibt das Zahlenformat für automatisch nummerierte Endnoten an. |
| [Position](../../aspose.words.notes/endnoteoptions/position/) { get; set; } | Gibt die Position der Endnoten an. |
| [RestartRule](../../aspose.words.notes/endnoteoptions/restartrule/) { get; set; } | Legt fest, wann die automatische Nummerierung neu startet. |
| [StartNumber](../../aspose.words.notes/endnoteoptions/startnumber/) { get; set; } | Gibt die Startnummer oder das Anfangszeichen für die ersten automatisch nummerierten Endnoten an. |

## Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Endnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Endnote ist eine Möglichkeit, dem Text eine Referenz oder einen Randkommentar hinzuzufügen
 // das den Fluss des Haupttextes nicht beeinträchtigt.
// Beim Einfügen einer Endnote wird ein kleines hochgestelltes Referenzsymbol hinzugefügt
// am Haupttext, wo wir die Endnote einfügen.
// Jede Endnote erstellt auch einen Eintrag am Ende des Dokuments, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die „InsertEndnote“-Methode des Document Builders übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Wir können die Eigenschaft „Position“ verwenden, um zu bestimmen, wo das Dokument alle seine Endnoten platzieren wird.
// Wenn wir den Wert der Eigenschaft „Position“ auf „EndnotePosition.EndOfDocument“ setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Dokuments angezeigt. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „EndnotePosition.EndOfSection“ setzen,
// Jede Fußnote wird in einer Sammlung am Ende des Abschnitts angezeigt, dessen Text das Referenzzeichen der Endnote enthält.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
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

* property [EndnoteOptions](../../aspose.words/document/endnoteoptions/)
* property [EndnoteOptions](../../aspose.words/pagesetup/endnoteoptions/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
