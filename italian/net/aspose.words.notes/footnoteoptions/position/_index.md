---
title: FootnoteOptions.Position
second_title: Aspose.Words per .NET API Reference
description: FootnoteOptions proprietà. Specifica la posizione delle note a piè di pagina.
type: docs
weight: 30
url: /it/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Specifica la posizione delle note a piè di pagina.

```csharp
public FootnotePosition Position { get; set; }
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

### Guarda anche

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../footnoteoptions/)
* assemblea [Aspose.Words](../../../)


