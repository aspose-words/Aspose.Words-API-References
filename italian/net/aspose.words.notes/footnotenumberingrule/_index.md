---
title: FootnoteNumberingRule
second_title: Aspose.Words per .NET API Reference
description: Determina quando viene riavviata la numerazione automatica delle note a piè di pagina o di chiusura.
type: docs
weight: 4030
url: /it/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

Determina quando viene riavviata la numerazione automatica delle note a piè di pagina o di chiusura.

```csharp
public enum FootnoteNumberingRule
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Continuous | `0` | Numerazione continua in tutto il documento. |
| RestartSection | `1` | La numerazione ricomincia ad ogni sezione. |
| RestartPage | `2` | La numerazione ricomincia ad ogni pagina. Valido solo per le note a piè di pagina. |
| Default | `0` | UgualeContinuous . |

### Esempi

Mostra come riavviare la numerazione delle note a piè di pagina/note di chiusura in determinati punti del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento laterale al testo
// che non interferisce con il flusso del testo principale. 
// L'inserimento di una nota a piè di pagina/note di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// simbolo nel corpo principale del testo. Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ciascuna pagina che contiene
// i loro simboli di riferimento e le note di chiusura vengono visualizzati alla fine del documento.
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

// Per impostazione predefinita, il simbolo di riferimento per ciascuna nota a piè di pagina e nota di chiusura è il relativo indice
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e le note di chiusura e non riavvia questi conteggi in nessun momento.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Possiamo usare la proprietà "RestartRule" per riavviare il documento
// la nota a piè di pagina/la nota di chiusura viene conteggiata in una nuova pagina o sezione.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Guarda anche

* class [FootnoteOptions](../footnoteoptions)
* class [EndnoteOptions](../endnoteoptions)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->