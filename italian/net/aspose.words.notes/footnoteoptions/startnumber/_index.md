---
title: FootnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words per .NET
description: FootnoteOptions StartNumber proprietà. Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente in C#.
type: docs
weight: 50
url: /it/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente.

```csharp
public int StartNumber { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando[`RestartRule`](../restartrule/) è impostato su Continuous.

## Esempi

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

### Guarda anche

* class [FootnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
