---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Comment, il tuo strumento essenziale per gestire il testo dei commenti nei documenti. Migliora il tuo flusso di lavoro con un'integrazione perfetta!
type: docs
weight: 420
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
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Inizializza una nuova istanza di`Comment` classe. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Inizializza una nuova istanza di`Comment` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Restituisce il genitore`Comment`oggetto. Restituisce`null` per commenti di primo livello. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Restituisce o imposta il nome dell'autore per un commento. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Ottiene la data e l'ora in cui è stato fatto il commento. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Ottiene la data e l'ora UTC in cui è stato fatto il commento. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Ottiene o imposta il flag che indica che il commento è stato contrassegnato come completato. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di ancoraggio di questo oggetto. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Ottiene o imposta l'identificatore del commento. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Restituisce o imposta le iniziali dell'utente associato a un commento specifico. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | RestituisceComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Ottiene o imposta l'ID del commento padre. Un valore di`-1` significa che il commento non ha un genitore. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Restituisce una raccolta di`Comment` oggetti che sono figli immediati del commento specificato. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | RestituisceComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ottiene una raccolta di tabelle che sono figlie immediate della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore che ha visitato la fine del commento. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio del commento. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Aggiunge una risposta a questo commento. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Se l'ultimo elemento figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Rimuove tutte le risposte a questo commento. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Rimuove la risposta specificata a questo commento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Questo è un metodo comodo che consente di impostare facilmente il testo del commento. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Un commento è un'annotazione ancorata a una regione di testo o a una posizione nel testo. Un commento può contenere una quantità arbitraria di contenuto a livello di blocco.

Se un`Comment` l'oggetto si verifica da solo, il commento è ancorato a la posizione dell'`Comment` oggetto.

Per ancorare un commento a un'area di testo sono necessari tre oggetti:`Comment` , [`CommentRangeStart`](../commentrangestart/) E[`CommentRangeEnd`](../commentrangeend/) Tutti e tre gli oggetti devono condividere lo stesso [`Id`](./id/) valore.

`Comment` è un nodo di livello inline e può essere solo un figlio di[`Paragraph`](../paragraph/).

`Comment` può contenere[`Paragraph`](../paragraph/) E[`Table`](../../aspose.words.tables/table/) nodi figlio.

## Esempi

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

 // In Microsoft Word, possiamo fare clic con il pulsante destro del mouse su questo commento nel corpo del documento per modificarlo o per rispondere.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Mostra come aggiungere un commento a un documento e poi rispondere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Posiziona il commento in un nodo del corpo del documento.
// Questo commento verrà visualizzato nella posizione del suo paragrafo,
// fuori dal margine destro della pagina e con una linea tratteggiata che lo collega al suo paragrafo.
builder.CurrentParagraph.AppendChild(comment);

// Aggiungi una risposta, che verrà visualizzata sotto il commento padre.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Sia i commenti che le risposte sono nodi Commento.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// I commenti che non rispondono ad altri commenti sono di "livello superiore". Non hanno commenti precedenti.
Assert.Null(comment.Ancestor);

// Le risposte hanno un commento di primo livello antenato.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Guarda anche

* class [InlineStory](../inlinestory/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
