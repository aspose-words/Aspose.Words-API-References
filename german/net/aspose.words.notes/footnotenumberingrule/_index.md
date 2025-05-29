---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words FootnoteNumberingRule-Aufzählung zur Steuerung der automatischen Fuß- und Endnotennummerierung. Optimieren Sie mühelos die Formatierung Ihres Dokuments!
type: docs
weight: 4960
url: /de/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Bestimmt, wann die automatische Fußnoten- oder Endnotennummerierung neu gestartet wird.

```csharp
public enum FootnoteNumberingRule
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Continuous | `0` | Nummerierung fortlaufend im gesamten Dokument. |
| RestartSection | `1` | Die Nummerierung beginnt bei jedem Abschnitt neu. |
| RestartPage | `2` | Die Nummerierung beginnt auf jeder Seite neu. Gilt nur für Fußnoten. |
| Default | `0` | GleichContinuous . |

## Beispiele

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
