---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words per .NET
description: Document JoinRunsWithSameFormatting metodo. I join vengono eseguiti con la stessa formattazione in tutti i paragrafi del documento in C#.
type: docs
weight: 620
url: /it/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

I join vengono eseguiti con la stessa formattazione in tutti i paragrafi del documento.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valore di ritorno

Numero di unioni eseguite. Quando**N** le piste adiacenti vengono unite come contano**N-1** si unisce.

## Osservazioni

Questo è un metodo di ottimizzazione. Alcuni documenti contengono sequenze adiacenti con la stessa formattazione. Di solito ciò si verifica se un documento è stato modificato manualmente in modo intensivo. È possibile ridurre le dimensioni del documento e accelerare l'ulteriore elaborazione unendo queste sequenze.

L'operazione controlla ogni[`Paragraph`](../../paragraph/) nodo nel documento per adiacente[`Run`](../../run/) nodi con proprietà identiche. Ignora gli identificatori univoci utilizzati per tenere traccia delle sessioni di modifica della creazione e della modifica di run . La prima esecuzione in ogni sequenza di unione accumula tutto il testo. Le esecuzioni rimanenti vengono eliminate dal documento.

## Esempi

Mostra come unire le esecuzioni in un documento per ridurre le esecuzioni non necessarie.

```csharp
// Apre un documento che contiene sequenze di testo adiacenti con formattazione identica,
// che si verifica comunemente se modifichiamo più volte lo stesso paragrafo in Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Se un numero qualsiasi di queste esecuzioni sono adiacenti con formattazione identica,
// allora il documento può essere semplificato.
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
