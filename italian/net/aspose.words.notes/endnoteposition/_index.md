---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words EndnotePosition per un controllo preciso sul posizionamento delle note di chiusura nei documenti, migliorando le tue capacità di formattazione del testo.
type: docs
weight: 4940
url: /it/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Definisce la posizione della nota di chiusura.

```csharp
public enum EndnotePosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EndOfSection | `0` | Le note di chiusura vengono visualizzate alla fine della sezione. |
| EndOfDocument | `3` | Le note di chiusura vengono visualizzate alla fine del documento. |

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

* class [EndnoteOptions](../endnoteoptions/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
