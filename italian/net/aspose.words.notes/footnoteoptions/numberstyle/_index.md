---
title: FootnoteOptions.NumberStyle
second_title: Aspose.Words per .NET API Reference
description: FootnoteOptions proprietà. Specifica il formato numerico per le note a piè di pagina numerate automaticamente.
type: docs
weight: 20
url: /it/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

Specifica il formato numerico per le note a piè di pagina numerate automaticamente.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### Osservazioni

Non tutti gli stili numerici sono applicabili per questa proprietà. Per l'elenco degli stili numerici applicabili , vedere la finestra di dialogo Inserisci nota a piè di pagina o nota di chiusura in Microsoft Word. Se si seleziona uno stile numerico non applicabile, Microsoft Word tornerà a un valore predefinito.

### Esempi

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

### Guarda anche

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../footnoteoptions/)
* assemblea [Aspose.Words](../../../)


