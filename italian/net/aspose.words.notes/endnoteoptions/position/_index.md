---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words per .NET
description: Scopri come la proprietà Posizione di EndnoteOptions migliora il layout del tuo documento specificando la posizione ideale per le note di chiusura. Ottimizza la tua scrittura oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Specifica la posizione delle note di chiusura.

```csharp
public EndnotePosition Position { get; set; }
```

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

### Guarda anche

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
