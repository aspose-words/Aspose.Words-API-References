---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Inline, progettata per la formattazione dei caratteri nei nodi inline. Migliora lo stile del tuo documento senza nodi figlio!
type: docs
weight: 3710
url: /it/net/aspose.words/inline/
---
## Inline class

Classe base per nodi di livello inline a cui è possibile associare la formattazione dei caratteri, ma non possono avere nodi figlio propri.

Per saperne di più, visita il[Livelli logici dei nodi in un documento](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) articolo di documentazione.

```csharp
public abstract class Inline : Node
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ottiene il tipo di questo nodo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Una classe derivata da`Inline` può essere un figlio di[`Paragraph`](../paragraph/).

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

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
