---
title: Inline
second_title: Aspose.Words per .NET API Reference
description: Classe base per nodi a livello inline che possono avere la formattazione dei caratteri associata ma non possono avere nodi figlio propri.
type: docs
weight: 3060
url: /it/net/aspose.words/inline/
---
## Inline class

Classe base per nodi a livello inline che possono avere la formattazione dei caratteri associata, ma non possono avere nodi figlio propri.

```csharp
public abstract class Inline : Node
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce vero se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce **VERO** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ottiene il tipo di questo nodo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Una classe derivata da **In linea** può essere un figlio di **Paragrafo**.

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

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
