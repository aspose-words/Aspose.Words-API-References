---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words für .NET
description: PageSetup EndnoteOptions eigendom. Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Endnoten in diesem Abschnitt in C#.
type: docs
weight: 120
url: /de/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Endnoten in diesem Abschnitt.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Beispiele

Zeigt, wie Optionen konfiguriert werden, die sich auf Fußnoten/Endnoten in einem Abschnitt auswirken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Alle Fußnoten im ersten Abschnitt so konfigurieren, dass die Nummerierung bei 1 beginnt
// auf jeder neuen Seite und werden auf jeder Seite direkt unter dem Text angezeigt.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Konfigurieren Sie alle Endnoten im ersten Abschnitt, um eine kontinuierliche Zählung im gesamten Abschnitt aufrechtzuerhalten.
// beginnend bei 1. Legen Sie außerdem fest, dass alle am Ende des Dokuments gesammelt angezeigt werden.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Siehe auch

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
