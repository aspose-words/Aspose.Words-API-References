---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.DocumentDirection per controllare facilmente il flusso di testo nei tuoi documenti. Migliora la leggibilità e la formattazione con questa potente funzionalità!
type: docs
weight: 4030
url: /it/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Consente di specificare la direzione in cui far scorrere il testo in un documento.

```csharp
public enum DocumentDirection
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| LeftToRight | `0` | Direzione da sinistra a destra. |
| RightToLeft | `1` | Direzione da destra a sinistra. |
| Auto | `2` | Rilevamento automatico della direzione. |

## Esempi

Mostra come rilevare la direzione del testo in un documento di testo normale.

```csharp
// Creiamo un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" rileva automaticamente
// la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo normale.
// La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Rileva il testo ebraico come scritto da destra a sinistra.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Rileva il testo inglese come scritto da destra a sinistra.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
