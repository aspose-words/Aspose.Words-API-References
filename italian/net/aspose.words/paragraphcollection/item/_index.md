---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a paragrafi specifici con la proprietà ParagraphCollection Item. Recupera qualsiasi paragrafo tramite indice per una gestione fluida del testo.
type: docs
weight: 10
url: /it/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Recupera un[`Paragraph`](../../paragraph/) all'indice dato.

```csharp
public Paragraph this[int index] { get; }
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

Mostra come verificare se un paragrafo è una revisione di spostamento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Questo documento contiene revisioni "Sposta", che appaiono quando evidenziamo il testo con il cursore,
// e quindi trascinalo per spostarlo in un'altra posizione
// durante il monitoraggio delle revisioni in Microsoft Word tramite "Revisione" -> "Traccia modifiche".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Le revisioni di spostamento sono costituite da coppie di revisioni "Sposta da" e "Sposta a".
// Queste revisioni sono potenziali modifiche al documento che possiamo accettare o rifiutare.
// Prima di accettare/rifiutare una revisione di spostamento, il documento
// deve tenere traccia sia della destinazione di partenza che di quella di arrivo del testo.
// Il secondo e il quarto paragrafo definiscono una di tali revisioni e pertanto hanno entrambi lo stesso contenuto.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La revisione "Sposta da" è il paragrafo da cui abbiamo trascinato il testo.
// Se accettiamo la revisione, questo paragrafo scomparirà,
// e l'altro rimarrà e non sarà più una revisione.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La revisione "Sposta in" è il paragrafo in cui abbiamo trascinato il testo.
// Se rifiutiamo la revisione, questo paragrafo scomparirà e l'altro rimarrà.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Guarda anche

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
