---
title: EndnoteOptions.Position
second_title: Aspose.Words per .NET API Reference
description: EndnoteOptions proprietà. Specifica la posizione delle note di chiusura.
type: docs
weight: 20
url: /it/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Specifica la posizione delle note di chiusura.

```csharp
public EndnotePosition Position { get; set; }
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

### Guarda anche

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../endnoteoptions/)
* assemblea [Aspose.Words](../../../)


