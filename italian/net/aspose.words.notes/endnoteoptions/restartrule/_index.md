---
title: EndnoteOptions.RestartRule
second_title: Aspose.Words per .NET API Reference
description: EndnoteOptions proprietà. Determina quando riavvia la numerazione automatica.
type: docs
weight: 30
url: /it/net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

Determina quando riavvia la numerazione automatica.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

### Osservazioni

Non tutti i valori sono applicabili alle note di chiusura. Per verificare quali valori sono applicabili, vedere[`FootnoteNumberingRule`](../../footnotenumberingrule/).

### Esempi

Mostra come riavviare la numerazione delle note a piè di pagina/note di chiusura in determinati punti del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento a margine del testo
 // che non interferisca con il flusso del corpo principale del testo.
// L'inserimento di una nota a piè di pagina/nota finale aggiunge un piccolo simbolo di riferimento in apice
// nel corpo principale del testo dove inseriamo la nota a piè di pagina/nota finale.
// Ogni nota a piè di pagina/nota finale crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// simbolo nel corpo del testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ciascuna pagina che contiene
// i loro simboli di riferimento e le note finali vengono visualizzati alla fine del documento.
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

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e di chiusura e non riavvia questi conteggi in nessun momento.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Possiamo utilizzare la proprietà "RestartRule" per riavviare il documento
// la nota a piè di pagina/nota finale conta in una nuova pagina o sezione.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Guarda anche

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../endnoteoptions/)
* assemblea [Aspose.Words](../../../)


