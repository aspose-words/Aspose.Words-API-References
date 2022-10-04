---
title: FootnoteOptions
second_title: Aspose.Words per .NET API Reference
description: Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento.
type: docs
weight: 150
url: /it/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### Esempi

Mostra come selezionare una posizione diversa in cui il documento raccoglie e visualizza le note a piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota a piè di pagina è un modo per allegare un riferimento o un commento laterale al testo
// che non interferisce con il flusso del testo principale.  
// L'inserimento di una nota a piè di pagina aggiunge un piccolo simbolo di riferimento in apice
// al corpo del testo principale dove inseriamo la nota a piè di pagina.
// Ogni nota a piè di pagina crea anche una voce in fondo alla pagina, composta da un simbolo
// che corrisponde al simbolo di riferimento nel corpo principale del testo.
// Il testo di riferimento che passiamo al metodo "InsertFootnote" del generatore di documenti.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Possiamo usare la proprietà "Posizione" per determinare dove il documento collocherà tutte le sue note a piè di pagina.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BottomOfPage",
// ogni nota a piè di pagina apparirà in fondo alla pagina che contiene il suo segno di riferimento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BeneathText",
// ogni nota a piè di pagina apparirà alla fine del testo della pagina che contiene il suo segno di riferimento.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Mostra come impostare un numero in corrispondenza del quale il documento inizia il conteggio delle note a piè di pagina/note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento laterale al testo
// che non interferisce con il flusso del testo principale. 
// L'inserimento di una nota a piè di pagina/note di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo
// che corrisponde al simbolo di riferimento nel corpo principale del testo.
// Il testo di riferimento che passiamo al metodo "InsertEndnote" del generatore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ciascuna pagina che contiene
// i loro simboli di riferimento e le note di chiusura vengono visualizzati alla fine del documento.
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

// Per impostazione predefinita, il simbolo di riferimento per ciascuna nota a piè di pagina e nota di chiusura è il relativo indice
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura, che iniziano entrambe con 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Possiamo usare la proprietà "StartNumber" per ottenere il documento
// inizia il conteggio di una nota a piè di pagina o di chiusura con un numero diverso.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Mostra come modificare lo stile numerico dei segni di riferimento di note a piè di pagina/note di chiusura.

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Per impostazione predefinita, il simbolo di riferimento per ciascuna nota a piè di pagina e nota di chiusura è il relativo indice
// tra tutte le note a piè di pagina/note di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura. Per impostazione predefinita, le note a piè di pagina mostrano i loro numeri utilizzando numeri arabi,
// e le note di chiusura mostrano i loro numeri in numeri romani minuscoli.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Possiamo usare la proprietà "NumberStyle" per applicare stili di numerazione personalizzati a note a piè di pagina e note di chiusura.
// Ciò non influirà sulle note a piè di pagina/note di chiusura con segni di riferimento personalizzati.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

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

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
