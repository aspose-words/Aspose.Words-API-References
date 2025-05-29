---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words per .NET
description: Scopri come il metodo JoinRunsWithSameFormatting unisce perfettamente il testo formattato nei paragrafi del tuo documento, conferendogli un aspetto curato e professionale.
type: docs
weight: 660
url: /it/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Unisce le esecuzioni con la stessa formattazione in tutti i paragrafi del documento.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valore di ritorno

Numero di join eseguiti. Quando**N** le corse adiacenti vengono unite e contano come**N - 1** si unisce.

## Osservazioni

Questo è un metodo di ottimizzazione. Alcuni documenti contengono esecuzioni adiacenti con la stessa formattazione. Di solito questo si verifica se un documento è stato modificato manualmente in modo intensivo. È possibile ridurre le dimensioni del documento e velocizzare l'ulteriore elaborazione unendo queste esecuzioni.

L'operazione controlla ogni[`Paragraph`](../../paragraph/) nodo nel documento per adiacente[`Run`](../../run/)Nodi con proprietà identiche. Ignora gli identificatori univoci utilizzati per tracciare le sessioni di creazione e modifica di run . La prima esecuzione in ogni sequenza di join accumula tutto il testo. Le restanti esecuzioni vengono eliminate dal documento.

## Esempi

Mostra come unire le esecuzioni in un documento per ridurre quelle non necessarie.

```csharp
// Aprire un documento che contiene sequenze di testo adiacenti con formattazione identica,
// cosa che accade spesso se modifichiamo lo stesso paragrafo più volte in Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Se un numero qualsiasi di queste esecuzioni sono adiacenti con formattazione identica,
// quindi il documento può essere semplificato.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Combina tali esecuzioni con questo metodo e verifica il numero di unioni di esecuzioni che avranno luogo.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Il numero di join e il numero di esecuzioni che abbiamo dopo il join
// dovrebbe sommare il numero di esecuzioni effettuate inizialmente.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
