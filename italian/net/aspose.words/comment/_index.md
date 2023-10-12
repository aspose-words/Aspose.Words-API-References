---
title: Class Comment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Comment classe. Rappresenta un contenitore per il testo di un commento.
type: docs
weight: 230
url: /it/net/aspose.words/comment/
---
## Comment class

Rappresenta un contenitore per il testo di un commento.

Per saperne di più, visita il[Lavorare con i commenti](https://docs.aspose.com/words/net/working-with-comments/) articolo di documentazione.

```csharp
public sealed class Comment : InlineStory
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Inizializza una nuova istanza di`Comment` classe. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Inizializza una nuova istanza di`Comment` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Restituisce il genitore`Comment` oggetto. ritorna`nullo` per commenti di primo livello. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Restituisce o imposta il nome dell'autore per un commento. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Ottiene la data e l'ora in cui è stato creato il commento. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Ottiene o imposta un flag che indica che il commento è stato contrassegnato come completato. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Fornisce l'accesso alla formattazione del carattere del carattere di ancoraggio di questo oggetto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Ottiene l'identificatore del commento. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Restituisce o imposta le iniziali dell'utente associato ad uno specifico commento. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Restituisce vero se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | RestituisceComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Restituisce una raccolta di`Comment` oggetti che sono figli immediati del commento specificato. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | RestituisceComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ottiene una raccolta di tabelle che sono figli immediati della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(DocumentVisitor) |  |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Aggiunge una risposta a questo commento. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
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
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Rimuove tutte le risposte a questo commento. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Rimuove la risposta specificata a questo commento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [SetText](../../aspose.words/comment/settext/)(string) | Questo è un metodo comodo che consente di impostare facilmente il testo del commento. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Un commento è un'annotazione ancorata a una regione di testo o a una posizione nel testo. Un commento può contenere una quantità arbitraria di contenuto a livello di blocco.

Se un`Comment` oggetto si verifica da solo, il commento è ancorato alla posizione del`Comment` oggetto.

Per ancorare un commento ad una regione di testo sono necessari tre oggetti:`Comment` , [`CommentRangeStart`](../commentrangestart/) E[`CommentRangeEnd`](../commentrangeend/) . Tutti e tre gli oggetti devono condividere lo stesso [`Id`](./id/) valore.

`Comment` è un nodo a livello inline e può essere solo figlio di[`Paragraph`](../paragraph/).

`Comment` può contenere[`Paragraph`](../paragraph/) E[`Table`](../../aspose.words.tables/table/) nodi figli.

### Esempi

Mostra come aggiungere un commento a un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // In Microsoft Word, possiamo fare clic con il pulsante destro del mouse su questo commento nel corpo del documento per modificarlo o rispondere.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Mostra come aggiungere un commento a un documento e quindi rispondere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Posiziona il commento in un nodo nel corpo del documento.
// Questo commento verrà visualizzato nella posizione del suo paragrafo,
// fuori dal margine destro della pagina e con una linea tratteggiata che lo collega al paragrafo.
builder.CurrentParagraph.AppendChild(comment);

// Aggiunge una risposta, che verrà visualizzata sotto il commento principale.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Commenti e risposte sono entrambi nodi Commento.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// I commenti che non rispondono ad altri commenti sono di "livello superiore". Non hanno commenti sugli antenati.
Assert.Null(comment.Ancestor);

// Le risposte hanno un commento di livello superiore antenato.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Guarda anche

* class [InlineStory](../inlinestory/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


