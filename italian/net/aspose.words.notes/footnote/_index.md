---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Notes.Footnote, il tuo strumento essenziale per gestire con facilità e precisione le note a piè di pagina e le note di chiusura nei tuoi documenti.
type: docs
weight: 4950
url: /it/net/aspose.words.notes/footnote/
---
## Footnote class

Rappresenta un contenitore per il testo di una nota a piè di pagina o di una nota di chiusura.

Per saperne di più, visita il[Lavorare con note a piè di pagina e note di chiusura](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) articolo di documentazione.

```csharp
public class Footnote : InlineStory
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | Inizializza un'istanza di`Footnote` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ActualReferenceMark](../../aspose.words.notes/footnote/actualreferencemark/) { get; } | Ottiene il testo effettivo del segno di riferimento visualizzato nel documento per questa nota a piè di pagina. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di ancoraggio di questo oggetto. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di una nota di chiusura. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Contiene un valore che specifica se si tratta di una nota a piè di pagina numerata automaticamente o di una nota a piè di pagina con segno di riferimento personalizzato definito dall'utente. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | RestituisceFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Ottiene/imposta il segno di riferimento personalizzato da utilizzare per questa nota a piè di pagina. Il valore predefinito è **stringa vuota** (Empty ), il che significa che vengono utilizzate note a piè di pagina numerate automaticamente. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | RestituisceFootnotes OEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ottiene una raccolta di tabelle che sono figlie immediate della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato la fine della nota a piè di pagina. |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio della nota a piè di pagina. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Se l'ultimo elemento figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

IL`Footnote` La classe viene utilizzata per rappresentare sia le note a piè di pagina che quelle di chiusura in un documento Word.

`Footnote` è un nodo di livello inline e può essere solo un figlio di[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` può contenere[`Paragraph`](../../aspose.words/paragraph/) E[`Table`](../../aspose.words.tables/table/) nodi figlio.

## Esempi

Mostra come inserire e personalizzare le note a piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi del testo e fai riferimento ad esso con una nota a piè di pagina. Questa nota inserirà un piccolo riferimento in apice.
// contrassegna dopo il testo a cui fa riferimento e crea una voce sotto il testo principale in fondo alla pagina.
// Questa voce conterrà il segno di riferimento della nota a piè di pagina e il testo di riferimento,
// che passeremo al metodo "InsertFootnote" del generatore di documenti.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Se questa proprietà è impostata su "true", il segno di riferimento della nostra nota a piè di pagina
// sarà il suo indice tra tutte le note a piè di pagina della sezione.
// Questa è la prima nota a piè di pagina, quindi il segno di riferimento sarà "1".
Assert.True(footnote.IsAuto);

 // Possiamo spostare il generatore di documenti all'interno della nota a piè di pagina per modificarne il testo di riferimento.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Possiamo impostare un segno di riferimento personalizzato che la nota a piè di pagina utilizzerà al posto del suo numero di indice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un segnalibro con il flag "IsAuto" impostato su true mostrerà comunque il suo indice reale
// anche se i segnalibri precedenti visualizzano riferimenti personalizzati, il riferimento di questo segnalibro sarà "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Guarda anche

* class [InlineStory](../../aspose.words/inlinestory/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
