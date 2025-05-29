---
title: InlineStory.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsMoveFromRevision di InlineStory. Tieni traccia facilmente dei contenuti spostati o eliminati in Microsoft Word con il monitoraggio delle modifiche abilitato per una modifica fluida.
type: docs
weight: 50
url: /it/net/aspose.words/inlinestory/ismovefromrevision/
---
## InlineStory.IsMoveFromRevision property

Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato.

```csharp
public bool IsMoveFromRevision { get; }
```

## Esempi

Mostra come visualizzare le proprietà relative alla revisione dei nodi InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Quando modifichiamo il documento mentre è attiva l'opzione "Revisioni", che si trova in Revisione -> Monitoraggio,
// è attivato in Microsoft Word, le modifiche che applichiamo vengono considerate revisioni.
// Quando si modifica un documento utilizzando Aspose.Words, possiamo iniziare a monitorare le revisioni
// richiamando il metodo "StartTrackRevisions" del documento e interrompendo il monitoraggio tramite il metodo "StopTrackRevisions".
// Possiamo accettare le revisioni per assimilarle al documento
// oppure rifiutarli per annullare e scartare la modifica proposta.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo InlineStory.
// 1 - Una revisione "inserisci":
// Questa revisione si verifica quando inseriamo del testo durante il monitoraggio delle modifiche.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Una revisione "da passare":
// Quando evidenziamo il testo in Microsoft Word e poi lo trasciniamo in un punto diverso del documento
// durante il monitoraggio delle modifiche, vengono visualizzate due revisioni.
// La revisione "da spostare" è una copia del testo originale prima che lo spostassimo.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Una revisione "passa a":
// La revisione "sposta in" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// Le revisioni "Sposta da" e "Sposta a" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// L'accettazione di una revisione di spostamento elimina la revisione "da cui si sposta" e il suo testo,
// e mantiene il testo della revisione "sposta a".
// Rifiutando una revisione di spostamento, al contrario, viene mantenuta la revisione "da spostare" ed eliminata la revisione "a spostare".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Una revisione "eliminata":
// Questa revisione si verifica quando eliminiamo del testo durante il monitoraggio delle modifiche. Quando eliminiamo del testo in questo modo,
// rimarrà nel documento come revisione finché non accetteremo la revisione,
// che eliminerà definitivamente il testo, oppure rifiuterà la revisione, che manterrà il testo eliminato dov'era.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Guarda anche

* class [InlineStory](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
