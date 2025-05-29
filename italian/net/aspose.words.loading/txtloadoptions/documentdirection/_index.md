---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words per .NET
description: Scopri la proprietà DocumentDirection di TxtLoadOptions per impostare facilmente la direzione del documento. Ottimizza il tuo layout con l'impostazione predefinita LeftToRight!
type: docs
weight: 50
url: /it/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Ottiene o imposta una direzione del documento. Il valore predefinito èLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

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

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
