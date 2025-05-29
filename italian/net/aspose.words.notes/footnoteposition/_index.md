---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Notes.FootnotePosition per personalizzare il posizionamento delle note a piè di pagina, migliorando la formattazione e la leggibilità del documento.
type: docs
weight: 4980
url: /it/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Definisce la posizione della nota a piè di pagina.

```csharp
public enum FootnotePosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| BottomOfPage | `1` | Le note a piè di pagina vengono visualizzate in fondo a ogni pagina. |
| BeneathText | `2` | Le note a piè di pagina vengono visualizzate sotto il testo in ogni pagina. |

## Esempi

Mostra come selezionare una posizione diversa in cui il documento raccoglie e visualizza le note a piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una nota a piè di pagina è un modo per allegare un riferimento o un commento laterale al testo
 // che non interferisca con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina aggiunge un piccolo simbolo di riferimento in apice
// nel corpo del testo principale dove inseriamo la nota a piè di pagina.
// Ogni nota a piè di pagina crea anche una voce in fondo alla pagina, costituita da un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo "InsertFootnote" del generatore di documenti.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Possiamo usare la proprietà "Posizione" per determinare dove verranno posizionate tutte le note a piè di pagina del documento.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BottomOfPage",
// ogni nota a piè di pagina verrà visualizzata in fondo alla pagina che contiene il relativo riferimento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BeneathText",
// ogni nota a piè di pagina verrà visualizzata alla fine del testo della pagina che contiene il relativo segno di riferimento.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Guarda anche

* class [FootnoteOptions](../footnoteoptions/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
