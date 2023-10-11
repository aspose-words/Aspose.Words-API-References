---
title: RunCollection.Item
second_title: Aspose.Words per .NET API Reference
description: RunCollection proprietà. Recupera aRun allindice indicato.
type: docs
weight: 10
url: /it/net/aspose.words/runcollection/item/
---
## RunCollection indexer

Recupera a[`Run`](../../run/) all'indice indicato.

```csharp
public Run this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta. |

### Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 significa l'ultimo elemento, -2 significa il penultimo e così via.

Se indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento null.

Se indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento null.

### Esempi

Mostra come determinare il tipo di revisione di un nodo in linea.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Quando modifichiamo il documento mentre l'opzione "Traccia modifiche", che si trova in tramite Revisione -> Monitoraggio,
// è attivato in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Quando si modifica un documento utilizzando Aspose.Words, possiamo iniziare a tenere traccia delle revisioni in base a
// richiamando il metodo "StartTrackRevisions" del documento e interrompendo il tracciamento utilizzando il metodo "StopTrackRevisions".
// Possiamo accettare revisioni per integrarle nel documento
// o rifiutarli per modificare in modo efficace la modifica proposta.
Assert.AreEqual(6, doc.Revisions.Count);

// Il nodo padre di una revisione è l'esecuzione interessata dalla revisione. Una corsa è un nodo in linea.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo Inline.
// 1 - Una revisione "inserita":
// Questa revisione si verifica quando inseriamo del testo mentre teniamo traccia delle modifiche.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisione del "formato":
// Questa revisione si verifica quando modifichiamo la formattazione del testo mentre teniamo traccia delle modifiche.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisione "spostamento da":
// Quando evidenziamo il testo in Microsoft Word e quindi lo trasciniamo in una posizione diversa nel documento
// durante il monitoraggio delle modifiche, vengono visualizzate due revisioni.
// La revisione "sposta da" è una copia del testo originale prima che lo spostassimo.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisione "sposta in":
// La revisione "sposta in" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// Le revisioni "Sposta da" e "Sposta a" appaiono in coppia per ogni revisione di spostamento che effettuiamo.
// Accettare una revisione di spostamento elimina la revisione "sposta da" e il suo testo,
// e mantiene il testo della revisione "sposta in".
// Rifiutare una revisione di spostamento mantiene invece la revisione "sposta da" ed elimina la revisione "sposta in".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisione "elimina":
// Questa revisione si verifica quando eliminiamo il testo mentre teniamo traccia delle modifiche. Quando eliminiamo un testo come questo,
// rimarrà nel documento come revisione finché non accetteremo la revisione,
// che eliminerà il testo definitivamente o rifiuterà la revisione, che manterrà il testo che abbiamo eliminato dov'era.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Guarda anche

* class [Run](../../run/)
* class [RunCollection](../)
* spazio dei nomi [Aspose.Words](../../runcollection/)
* assemblea [Aspose.Words](../../../)


