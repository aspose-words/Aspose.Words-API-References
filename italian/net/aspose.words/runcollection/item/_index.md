---
title: RunCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a specifici elementi di RunCollection. Recupera qualsiasi Run tramite indice per una gestione semplificata dei dati e prestazioni migliorate.
type: docs
weight: 10
url: /it/net/aspose.words/runcollection/item/
---
## RunCollection indexer

Recupera un[`Run`](../../run/) all'indice dato.

```csharp
public Run this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice della collezione. |

## Osservazioni

L'indice è basato sullo zero.

Sono consentiti indici negativi che indicano l'accesso dalla parte posteriore della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, viene restituito un riferimento null.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, viene restituito un riferimento null.

## Esempi

Mostra come determinare il tipo di revisione di un nodo in linea.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Quando modifichiamo il documento mentre è attiva l'opzione "Revisioni", che si trova in Revisione -> Monitoraggio,
// è attivato in Microsoft Word, le modifiche che applichiamo vengono considerate revisioni.
// Quando si modifica un documento utilizzando Aspose.Words, possiamo iniziare a monitorare le revisioni
// richiamando il metodo "StartTrackRevisions" del documento e interrompendo il monitoraggio tramite il metodo "StopTrackRevisions".
// Possiamo accettare le revisioni per assimilarle al documento
// oppure rifiutarli per modificare in modo efficace la modifica proposta.
Assert.AreEqual(6, doc.Revisions.Count);

// Il nodo padre di una revisione è l'esecuzione a cui la revisione si riferisce. Un'esecuzione è un nodo inline.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo Inline.
// 1 - Una revisione "inserisci":
// Questa revisione si verifica quando inseriamo del testo durante il monitoraggio delle modifiche.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisione del "formato":
// Questa revisione si verifica quando modifichiamo la formattazione del testo durante il monitoraggio delle modifiche.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisione "da passare":
// Quando evidenziamo il testo in Microsoft Word e poi lo trasciniamo in un punto diverso del documento
// durante il monitoraggio delle modifiche, vengono visualizzate due revisioni.
// La revisione "da spostare" è una copia del testo originale prima che lo spostassimo.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisione "passa a":
// La revisione "sposta in" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// Le revisioni "Sposta da" e "Sposta a" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// L'accettazione di una revisione di spostamento elimina la revisione "da cui si sposta" e il suo testo,
// e mantiene il testo della revisione "sposta a".
// Rifiutando una revisione di spostamento, al contrario, viene mantenuta la revisione "da spostare" ed eliminata la revisione "a spostare".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisione "eliminata":
// Questa revisione si verifica quando eliminiamo del testo durante il monitoraggio delle modifiche. Quando eliminiamo del testo in questo modo,
// rimarrà nel documento come revisione finché non accetteremo la revisione,
// che eliminerà definitivamente il testo, oppure rifiuterà la revisione, che manterrà il testo eliminato dov'era.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Guarda anche

* class [Run](../../run/)
* class [RunCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
