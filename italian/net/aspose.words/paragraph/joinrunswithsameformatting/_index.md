---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words per .NET
description: Unisci senza sforzo le sequenze con una formattazione coerente nei tuoi paragrafi utilizzando il metodo JoinRunsWithSameFormatting. Migliora lo stile del tuo documento oggi stesso!
type: docs
weight: 300
url: /it/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Unisce le esecuzioni con la stessa formattazione nel paragrafo.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valore di ritorno

Numero di join eseguiti. Quando**N** le corse adiacenti vengono unite e contano come**N - 1** si unisce.

## Esempi

Mostra come semplificare i paragrafi unendo le sequenze superflue.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire quattro sequenze di testo nel paragrafo.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Se apriamo questo documento in Microsoft Word, il paragrafo apparirà come un unico corpo di testo senza soluzione di continuità.
// Tuttavia, sarà composto da quattro esecuzioni separate con la stessa formattazione. Paragrafi frammentati come questo
// può verificarsi quando si modificano manualmente parti di un paragrafo più volte in Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Modifica lo stile dell'ultima esecuzione per distinguerla dalle prime tre.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Possiamo eseguire il metodo "JoinRunsWithSameFormatting" per ottimizzare il contenuto del documento
// unendo serie simili in una sola, riducendone il conteggio complessivo.
// Questo metodo restituisce anche il numero di esecuzioni unite da questo metodo.
// Queste due fusioni si sono verificate per combinare le esecuzioni n. 1, n. 2 e n. 3,
// tralasciando l'Esecuzione n. 4 perché ha uno stile incompatibile.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Il numero di esecuzioni rimanenti sarà uguale al conteggio originale
// meno il numero di unioni eseguite dal metodo "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
