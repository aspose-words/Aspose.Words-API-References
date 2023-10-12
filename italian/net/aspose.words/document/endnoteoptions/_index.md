---
title: Document.EndnoteOptions
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Fornisce opzioni che controllano la numerazione e il posizionamento delle note di chiusura in questo documento.
type: docs
weight: 110
url: /it/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Fornisce opzioni che controllano la numerazione e il posizionamento delle note di chiusura in questo documento.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

### Esempi

Mostra come selezionare una posizione diversa in cui il documento raccoglie e visualizza le sue note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota finale è un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del corpo principale del testo.
// L'inserimento di una nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo principale del testo dove inseriamo la nota finale.
// Ogni nota finale crea anche una voce alla fine del documento, costituita da un simbolo
// che corrisponde al simbolo di riferimento nel corpo del testo principale.
// Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Possiamo usare la proprietà "Posizione" per determinare dove il documento posizionerà tutte le sue note di chiusura.
// Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfDocument",
// ogni nota a piè di pagina verrà visualizzata in una raccolta alla fine del documento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà "Position" su "EndnotePosition.EndOfSection",
// ogni nota a piè di pagina verrà visualizzata in una raccolta alla fine della sezione il cui testo contiene il segno di riferimento della nota finale.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

Mostra come impostare un numero con il quale il documento inizia il conteggio delle note a piè di pagina/note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento a margine del testo
 // che non interferisca con il flusso del corpo principale del testo.
// L'inserimento di una nota a piè di pagina/nota finale aggiunge un piccolo simbolo di riferimento in apice
// nel corpo principale del testo dove inseriamo la nota a piè di pagina/nota finale.
// Ogni nota a piè di pagina/nota finale crea anche una voce, che consiste in un simbolo
// che corrisponde al simbolo di riferimento nel corpo del testo principale.
// Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ciascuna pagina che contiene
// i loro simboli di riferimento e le note finali vengono visualizzati alla fine del documento.
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
// tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura, che iniziano entrambe con 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Possiamo utilizzare la proprietà "StartNumber" per ottenere il documento
// inizia il conteggio delle note a piè di pagina o di chiusura con un numero diverso.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Mostra come modificare lo stile dei numeri dei segni di riferimento delle note a piè di pagina/note di chiusura.

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
// tra tutte le note a piè di pagina/note finali del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura. Per impostazione predefinita, le note a piè di pagina visualizzano i loro numeri utilizzando numeri arabi,
// e le note finali mostrano i loro numeri in numeri romani minuscoli.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Possiamo utilizzare la proprietà "NumberStyle" per applicare stili di numerazione personalizzati alle note a piè di pagina e alle note di chiusura.
// Ciò non influirà sulle note a piè di pagina/note di chiusura con segni di riferimento personalizzati.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

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

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


