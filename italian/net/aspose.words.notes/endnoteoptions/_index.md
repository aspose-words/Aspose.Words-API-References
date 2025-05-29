---
title: EndnoteOptions Class
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words per .NET
description: Scopri la classe EndnoteOptions di Aspose.Words per personalizzare la numerazione delle note di chiusura nei tuoi documenti e nelle tue sezioni. Migliora la formattazione dei tuoi documenti oggi stesso!
type: docs
weight: 4930
url: /it/net/aspose.words.notes/endnoteoptions/
---
## EndnoteOptions class

Rappresenta le opzioni di numerazione delle note di chiusura per un documento o una sezione.

Per saperne di più, visita il[Lavorare con note a piè di pagina e note di chiusura](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) articolo di documentazione.

```csharp
public sealed class EndnoteOptions
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [NumberStyle](../../aspose.words.notes/endnoteoptions/numberstyle/) { get; set; } | Specifica il formato numerico per le note di chiusura numerate automaticamente. |
| [Position](../../aspose.words.notes/endnoteoptions/position/) { get; set; } | Specifica la posizione delle note di chiusura. |
| [RestartRule](../../aspose.words.notes/endnoteoptions/restartrule/) { get; set; } | Determina quando riavviare la numerazione automatica. |
| [StartNumber](../../aspose.words.notes/endnoteoptions/startnumber/) { get; set; } | Specifica il numero o il carattere iniziale per le prime note finali numerate automaticamente. |

## Esempi

Mostra come selezionare una posizione diversa in cui il documento raccoglie e visualizza le note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota di chiusura è un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del testo principale.
// L'inserimento di una nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota di chiusura.
// Ogni nota di chiusura crea anche una voce alla fine del documento, costituita da un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Possiamo usare la proprietà "Posizione" per determinare dove verranno posizionate tutte le note di chiusura del documento.
// Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfDocument",
// ogni nota a piè di pagina verrà visualizzata in una raccolta alla fine del documento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfSection",
// ogni nota a piè di pagina verrà visualizzata in una raccolta alla fine della sezione il cui testo contiene il segno di riferimento della nota di chiusura.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

Mostra come impostare un numero in base al quale il documento inizia il conteggio delle note a piè di pagina/note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i relativi simboli di riferimento e le note di chiusura vengono visualizzati alla fine del documento.
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

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note finali, che iniziano entrambe da 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Possiamo usare la proprietà "StartNumber" per ottenere il documento
// inizia il conteggio delle note a piè di pagina o delle note di chiusura da un numero diverso.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Mostra come modificare lo stile dei numeri dei riferimenti delle note a piè di pagina/note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// simbolo nel corpo del testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i relativi simboli di riferimento e le note di chiusura vengono visualizzati alla fine del documento.
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

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura. Per impostazione predefinita, le note a piè di pagina visualizzano i numeri arabi,
// e le note finali mostrano i numeri in numeri romani minuscoli.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Possiamo usare la proprietà "NumberStyle" per applicare stili di numerazione personalizzati alle note a piè di pagina e alle note di chiusura.
// Ciò non influirà sulle note a piè di pagina/note di chiusura con riferimenti personalizzati.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Mostra come riavviare la numerazione delle note a piè di pagina/note di chiusura in determinati punti del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note finali sono un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// simbolo nel corpo del testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i relativi simboli di riferimento e le note di chiusura vengono visualizzati alla fine del documento.
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
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e le note di chiusura e non riavvia questi conteggi in nessun punto.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Possiamo usare la proprietà "RestartRule" per riavviare il documento
// la nota a piè di pagina/nota di chiusura viene conteggiata in una nuova pagina o sezione.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Guarda anche

* property [EndnoteOptions](../../aspose.words/document/endnoteoptions/)
* property [EndnoteOptions](../../aspose.words/pagesetup/endnoteoptions/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
