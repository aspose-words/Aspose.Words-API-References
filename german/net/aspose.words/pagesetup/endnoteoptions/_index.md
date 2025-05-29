---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSetup EndnoteOptions“, um die Nummerierung und Positionierung von Endnoten einfach anzupassen und so die Dokumentformatierung und Übersichtlichkeit zu verbessern.
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

// Konfigurieren Sie alle Fußnoten im ersten Abschnitt so, dass die Nummerierung bei 1 neu beginnt
// auf jeder neuen Seite und werden auf jeder Seite direkt unter dem Text angezeigt.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Konfigurieren Sie alle Endnoten im ersten Abschnitt, um eine kontinuierliche Zählung im gesamten Abschnitt beizubehalten.
// beginnend bei 1. Stellen Sie außerdem alle so ein, dass sie gesammelt am Ende des Dokuments angezeigt werden.
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
