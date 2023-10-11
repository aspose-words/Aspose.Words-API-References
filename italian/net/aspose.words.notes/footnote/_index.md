---
title: Class Footnote
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Notes.Footnote classe. Rappresenta un contenitore per il testo di una nota a piè di pagina o di chiusura.
type: docs
weight: 4260
url: /it/net/aspose.words.notes/footnote/
---
## Footnote class

Rappresenta un contenitore per il testo di una nota a piè di pagina o di chiusura.

Per saperne di più, visita il[Lavorare con la nota a piè di pagina e la nota di chiusura](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) articolo di documentazione.

```csharp
public class Footnote : InlineStory
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Footnote](footnote/)(DocumentBase, FootnoteType) | Inizializza un'istanza di`Footnote` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Fornisce l'accesso alla formattazione del carattere del carattere di ancoraggio di questo oggetto. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di chiusura. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Contiene un valore che specifica se si tratta di una nota a piè di pagina con numerazione automatica o di una nota a piè di pagina con segno di riferimento personalizzato definito dall'utente. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | RestituisceFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../../aspose.words/range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Ottiene/imposta un segno di riferimento personalizzato da utilizzare per questa nota a piè di pagina. Il valore predefinito è **stringa vuota** (Empty ), il che significa che vengono utilizzate le note a piè di pagina con numerazione automatica. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | RestituisceFootnotes OEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ottiene una raccolta di tabelle che sono figli immediati della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(DocumentVisitor) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

IL`Footnote` La classe viene utilizzata per rappresentare sia le note a piè di pagina che le note di chiusura in un documento di Word.

`Footnote` è un nodo a livello inline e può essere solo figlio di[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` può contenere[`Paragraph`](../../aspose.words/paragraph/) E[`Table`](../../aspose.words.tables/table/) nodi figli.

### Esempi

Mostra come inserire e personalizzare le note a piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge testo e fa riferimento ad esso con una nota a piè di pagina. Questa nota inserirà un piccolo riferimento in apice
// segna dopo il testo a cui fa riferimento e crea una voce sotto il corpo del testo principale in fondo alla pagina.
// Questa voce conterrà il segno di riferimento della nota a piè di pagina e il testo di riferimento,
// che passeremo al metodo "InsertFootnote" del generatore di documenti.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Se questa proprietà è impostata su "true", allora il segno di riferimento della nostra nota a piè di pagina
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

// Possiamo impostare un segno di riferimento personalizzato che verrà utilizzato dalla nota a piè di pagina al posto del suo numero di indice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un segnalibro con il flag "IsAuto" impostato su true mostrerà comunque il suo indice reale
// anche se i segnalibri precedenti visualizzano segni di riferimento personalizzati, quindi il segno di riferimento di questo segnalibro sarà un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Guarda anche

* class [InlineStory](../../aspose.words/inlinestory/)
* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)


