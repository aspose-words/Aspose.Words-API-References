---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words per .NET
description: Scopri PageSetup FootnoteOptions per personalizzare facilmente la numerazione e il posizionamento delle note a piè di pagina, per una maggiore chiarezza e professionalità dei documenti.
type: docs
weight: 150
url: /it/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questa sezione.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## Esempi

Mostra come configurare le opzioni che influiscono sulle note a piè di pagina/note di chiusura in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configura tutte le note a piè di pagina nella prima sezione per riavviare la numerazione da 1
// in ogni nuova pagina e si visualizzano direttamente sotto il testo in ogni pagina.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Configura tutte le note di chiusura nella prima sezione per mantenere un conteggio continuo in tutta la sezione,
// a partire da 1. Inoltre, impostali tutti in modo che appaiano raccolti alla fine del documento.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Guarda anche

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
