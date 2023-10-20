---
title: InlineStory.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words per .NET
description: InlineStory IsMoveToRevision proprietà. RestituisceVERO se questo oggetto è stato spostato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato in C#.
type: docs
weight: 60
url: /it/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato.

```csharp
public bool IsMoveToRevision { get; }
```

## Esempi

Mostra come visualizzare le proprietà relative alla revisione dei nodi InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Quando modifichiamo il documento mentre l'opzione "Traccia modifiche", che si trova in tramite Revisione -> Monitoraggio,
// è attivato in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Quando si modifica un documento utilizzando Aspose.Words, possiamo iniziare a tenere traccia delle revisioni in base a
// richiamando il metodo "StartTrackRevisions" del documento e interrompendo il tracciamento utilizzando il metodo "StopTrackRevisions".
// Possiamo accettare revisioni per integrarle nel documento
// o rifiutarli per annullare e scartare la modifica proposta.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo InlineStory.
// 1 - Una revisione "inserita":
// Questa revisione si verifica quando inseriamo del testo mentre teniamo traccia delle modifiche.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Una revisione "spostamento da":
// Quando evidenziamo il testo in Microsoft Word e quindi lo trasciniamo in una posizione diversa nel documento
// durante il monitoraggio delle modifiche, vengono visualizzate due revisioni.
// La revisione "sposta da" è una copia del testo originale prima che lo spostassimo.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Una revisione "sposta in":
// La revisione "sposta in" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// Le revisioni "Sposta da" e "Sposta a" appaiono in coppia per ogni revisione di spostamento che effettuiamo.
// Accettare una revisione di spostamento elimina la revisione "sposta da" e il suo testo,
// e mantiene il testo della revisione "sposta in".
// Rifiutare una revisione di spostamento mantiene invece la revisione "sposta da" ed elimina la revisione "sposta in".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Una revisione "elimina":
// Questa revisione si verifica quando eliminiamo il testo mentre teniamo traccia delle modifiche. Quando eliminiamo un testo come questo,
// rimarrà nel documento come revisione finché non accetteremo la revisione,
// che eliminerà il testo definitivamente o rifiuterà la revisione, che manterrà il testo che abbiamo eliminato dov'era.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Guarda anche

* class [InlineStory](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
