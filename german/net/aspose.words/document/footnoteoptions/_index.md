---
title: FootnoteOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Fußnoten in diesem Dokument.
type: docs
weight: 150
url: /de/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Fußnoten in diesem Dokument.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### Beispiele

Zeigt, wie Sie einen anderen Ort auswählen, an dem das Dokument seine Fußnoten sammelt und anzeigt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Fußnote ist eine Möglichkeit, eine Referenz oder einen Seitenkommentar an einen Text anzuhängen
// das den Fluss des Haupttextes nicht stört.  
// Das Einfügen einer Fußnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erzeugt auch einen Eintrag am Ende der Seite, bestehend aus einem Symbol
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die "InsertFootnote"-Methode des Dokumenterstellers übergeben.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Wir können die Eigenschaft "Position" verwenden, um zu bestimmen, wo das Dokument alle seine Fußnoten platzieren wird.
// Wenn wir den Wert der Eigenschaft "Position" auf "FootnotePosition.BottomOfPage" setzen,
// Jede Fußnote wird unten auf der Seite angezeigt, die ihr Referenzzeichen enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft "Position" auf "FootnotePosition.BeneathText" setzen,
// jede Fußnote erscheint am Ende des Seitentextes, der ihr Referenzzeichen enthält.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Zeigt, wie Sie eine Zahl festlegen, bei der das Dokument mit der Fußnoten-/Endnotenzählung beginnt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, eine Referenz oder einen Nebenkommentar an Text anzuhängen
// das den Fluss des Haupttextes nicht stört. 
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt auch einen Eintrag, der aus einem Symbol besteht
// das mit dem Referenzsymbol im Haupttext übereinstimmt.
// Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenterstellers übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die enthält
// ihre Referenzsymbole und Endnoten erscheinen am Ende des Dokuments.
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
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument behält separate Zählungen bei
// für Fußnoten und für Endnoten, die beide bei 1 beginnen.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Wir können die Eigenschaft "StartNumber" verwenden, um das Dokument zu bekommen
// beginnt eine Fußnoten- oder Endnotenzählung bei einer anderen Nummer.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Zeigt, wie Sie den Nummernstil von Fußnoten-/Endnotenreferenzzeichen ändern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, eine Referenz oder einen Nebenkommentar an Text anzuhängen
// das den Fluss des Haupttextes nicht stört. 
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt auch einen Eintrag, der aus einem zur Referenz passenden Symbol besteht
// Symbol im Haupttext. Der Referenztext, den wir an die „InsertEndnote“-Methode des Dokumenterstellers übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die enthält
// ihre Referenzsymbole und Endnoten erscheinen am Ende des Dokuments.
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
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument behält separate Zählungen bei
// für Fußnoten und für Endnoten. Standardmäßig zeigen Fußnoten ihre Nummern mit arabischen Ziffern an,
// und Endnoten zeigen ihre Nummern in kleinen römischen Ziffern an.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Wir können die Eigenschaft "NumberStyle" verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Dies wirkt sich nicht auf Fußnoten/Endnoten mit benutzerdefinierten Referenzzeichen aus.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Zeigt, wie Sie die Fußnoten-/Endnotennummerierung an bestimmten Stellen im Dokument neu starten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, eine Referenz oder einen Nebenkommentar an Text anzuhängen
// das den Fluss des Haupttextes nicht stört. 
// Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// am Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erzeugt auch einen Eintrag, der aus einem zur Referenz passenden Symbol besteht
// Symbol im Haupttext. Der Referenztext, den wir an die „InsertEndnote“-Methode des Dokumenterstellers übergeben.
// Fußnoteneinträge werden standardmäßig unten auf jeder Seite angezeigt, die enthält
// ihre Referenzsymbole und Endnoten erscheinen am Ende des Dokuments.
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
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument behält separate Zählungen bei
// für Fußnoten und Endnoten und startet diese Zählungen an keiner Stelle neu.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Wir können die Eigenschaft "RestartRule" verwenden, um das Dokument neu zu starten
// die Fußnote/Endnote zählt auf einer neuen Seite oder einem neuen Abschnitt.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Siehe auch

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
