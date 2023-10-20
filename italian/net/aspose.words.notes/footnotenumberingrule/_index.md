---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words per .NET
description: Aspose.Words.Notes.FootnoteNumberingRule enum. Determina quando riavvia la numerazione automatica delle note a piè di pagina o delle note di chiusura in C#.
type: docs
weight: 4270
url: /it/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Determina quando riavvia la numerazione automatica delle note a piè di pagina o delle note di chiusura.

```csharp
public enum FootnoteNumberingRule
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Continuous | `0` | Numerazione continua in tutto il documento. |
| RestartSection | `1` | La numerazione ricomincia da ogni sezione. |
| RestartPage | `2` | La numerazione ricomincia da ogni pagina. Valido solo per le note a piè di pagina. |
| Default | `0` | UgualeContinuous . |

## Esempi

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
