---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words per .NET
description: Aspose.Words.Inline classe. Classe base per nodi a livello inline a cui può essere associata la formattazione dei caratteri ma non può avere nodi figlio propri in C#.
type: docs
weight: 3260
url: /it/net/aspose.words/inline/
---
## Inline class

Classe base per nodi a livello inline a cui può essere associata la formattazione dei caratteri, ma non può avere nodi figlio propri.

Per saperne di più, visita il[Livelli logici dei nodi in un documento](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) articolo di documentazione.

```csharp
public abstract class Inline : Node
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione dei caratteri di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ottiene il tipo di questo nodo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Una classe derivata da`Inline` può essere un figlio di[`Paragraph`](../paragraph/).

## Esempi

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

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
