---
title: IsDeleteRevision
second_title: Aspose.Words per .NET API Reference
description: Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche.
type: docs
weight: 20
url: /it/net/aspose.words/inline/isdeleterevision/
---
## Inline.IsDeleteRevision property

Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche.

```csharp
public bool IsDeleteRevision { get; }
```

### Esempi

Mostra come determinare il tipo di revisione di un nodo inline.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Quando modifichiamo il documento mentre l'opzione "Traccia modifiche", che si trova in tramite Revisione -> monitoraggio,
// è attivato in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Quando modifichiamo un documento usando Aspose.Words, possiamo iniziare a tenere traccia delle revisioni da
// richiamando il metodo "StartTrackRevisions" del documento e interrompendo il rilevamento utilizzando il metodo "StopTrackRevisions".
// Possiamo accettare revisioni per assimilarle al documento
// o rifiutarli per modificare in modo efficace la modifica proposta.
Assert.AreEqual(6, doc.Revisions.Count);

// Il nodo padre di una revisione è l'esecuzione che interessa la revisione. Una corsa è un nodo Inline.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo Inline.
// 1 - Una revisione "inserto":
// Questa revisione si verifica quando inseriamo del testo durante il rilevamento delle modifiche.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisione del "formato":
// Questa revisione si verifica quando modifichiamo la formattazione del testo durante il rilevamento delle modifiche.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisione "sposta da":
// Quando evidenziamo il testo in Microsoft Word, quindi lo trasciniamo in una posizione diversa nel documento
// durante il rilevamento delle modifiche, vengono visualizzate due revisioni.
// La revisione "sposta da" è una copia del testo originariamente prima dello spostamento.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisione "passa a":
// La revisione "sposta in" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// Le revisioni "Sposta da" e "Sposta in" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// L'accettazione di una revisione di spostamento elimina la revisione "sposta da" e il suo testo,
// e mantiene il testo della revisione "sposta in".
// Il rifiuto di una revisione di spostamento, al contrario, mantiene la revisione "sposta da" ed elimina la revisione "sposta in".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisione "cancella":
// Questa revisione si verifica quando eliminiamo il testo durante il rilevamento delle modifiche. Quando cancelliamo un testo come questo,
// rimarrà nel documento come revisione fino a quando non accettiamo la revisione,
// che cancellerà definitivamente il testo, o rifiuterà la revisione, che manterrà il testo che abbiamo eliminato dove era.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Guarda anche

* class [Inline](../../inline)
* spazio dei nomi [Aspose.Words](../../inline)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->