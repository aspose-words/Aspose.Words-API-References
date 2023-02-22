---
title: FootnoteOptions.RestartRule
second_title: Aspose.Words für .NET-API-Referenz
description: FootnoteOptions eigendom. Legt fest wann die automatische Nummerierung neu gestartet wird.
type: docs
weight: 40
url: /de/net/aspose.words.notes/footnoteoptions/restartrule/
---
## FootnoteOptions.RestartRule property

Legt fest, wann die automatische Nummerierung neu gestartet wird.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

### Beispiele

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

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [FootnoteOptions](../)
* namensraum [Aspose.Words.Notes](../../footnoteoptions/)
* Montage [Aspose.Words](../../../)


