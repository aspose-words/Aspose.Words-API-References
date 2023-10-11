---
title: PageSetup.EndnoteOptions
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Fornisce opzioni che controllano la numerazione e il posizionamento delle note di chiusura in questa sezione.
type: docs
weight: 120
url: /it/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Fornisce opzioni che controllano la numerazione e il posizionamento delle note di chiusura in questa sezione.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

### Esempi

Mostra come configurare le opzioni che influenzano le note a piè di pagina/note di chiusura in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configura tutte le note a piè di pagina nella prima sezione per riavviare la numerazione da 1
// ad ogni nuova pagina e vengono visualizzati direttamente sotto il testo su ogni pagina.
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

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


