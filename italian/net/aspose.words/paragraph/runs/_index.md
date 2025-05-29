---
title: Paragraph.Runs
linktitle: Runs
articleTitle: Runs
second_title: Aspose.Words per .NET
description: Scopri la proprietà Sequenze di paragrafo per accedere facilmente alle raccolte di testo formattato all'interno dei paragrafi, migliorando la struttura e la leggibilità del tuo documento.
type: docs
weight: 220
url: /it/net/aspose.words/paragraph/runs/
---
## Paragraph.Runs property

Fornisce l'accesso alla raccolta di testi digitati all'interno del paragrafo.

```csharp
public RunCollection Runs { get; }
```

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

* class [RunCollection](../../runcollection/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
