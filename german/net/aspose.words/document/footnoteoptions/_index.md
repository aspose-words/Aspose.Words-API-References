---
title: Document.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words für .NET
description: Erkunden Sie die Document FootnoteOptions-Eigenschaft, um die Nummerierung und Positionierung von Fußnoten anzupassen und so die Klarheit und Professionalität Ihres Dokuments zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Fußnoten in diesem Dokument.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Fußnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Fußnote ist eine Möglichkeit, einem Text einen Verweis oder einen Randkommentar hinzuzufügen.
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erzeugt auch einen Eintrag am Ende der Seite, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertFootnote“ des Dokumentgenerators übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Mit der Eigenschaft „Position“ können wir bestimmen, wo im Dokument alle Fußnoten platziert werden.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BottomOfPage“ setzen,
// Jede Fußnote wird unten auf der Seite angezeigt, die das entsprechende Referenzzeichen enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft „Position“ auf „FootnotePosition.BeneathText“ setzen,
// Jede Fußnote wird am Ende des Seitentextes angezeigt, der ihr Referenzzeichen enthält.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Zeigt, wie eine Zahl festgelegt wird, bei der im Dokument mit der Zählung der Fußnoten/Endnoten begonnen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt ebenfalls einen Eintrag, der aus einem Symbol besteht
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
// Fußnoteneinträge erscheinen standardmäßig am Ende jeder Seite, die Folgendes enthält:
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

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote der Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und für Endnoten, die beide bei 1 beginnen.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Wir können die Eigenschaft "StartNumber" verwenden, um das Dokument zu erhalten
// Beginnen Sie mit der Zählung einer Fuß- oder Endnote bei einer anderen Zahl.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Zeigt, wie der Nummerierungsstil von Fußnoten-/Endnotenverweiszeichen geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt ebenfalls einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
// Fußnoteneinträge erscheinen standardmäßig am Ende jeder Seite, die Folgendes enthält:
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

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote der Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und Endnoten. Standardmäßig werden Fußnoten mit arabischen Ziffern nummeriert,
// und Endnoten zeigen ihre Nummern in römischen Kleinbuchstaben an.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Wir können die Eigenschaft „NumberStyle“ verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Fußnoten/Endnoten mit benutzerdefinierten Referenzzeichen sind hiervon nicht betroffen.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Zeigt, wie die Fußnoten-/Endnotennummerierung an bestimmten Stellen im Dokument neu gestartet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an den Text anzuhängen
    // das den Textfluss des Hauptteils nicht beeinträchtigt.
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt ebenfalls einen Eintrag, der aus einem Symbol besteht, das mit der Referenz übereinstimmt
// Symbol im Haupttext. Der Referenztext, den wir an die Methode „InsertEndnote“ des Dokumentgenerators übergeben.
// Fußnoteneinträge erscheinen standardmäßig am Ende jeder Seite, die Folgendes enthält:
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

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote der Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument verwaltet separate Zählungen
// für Fußnoten und Endnoten und startet diese Zählungen zu keinem Zeitpunkt neu.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Wir können die Eigenschaft „RestartRule“ verwenden, um das Dokument neu zu starten
// Die Fußnote/Endnote zählt auf einer neuen Seite oder in einem neuen Abschnitt.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Siehe auch

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
