---
title: Story Class
linktitle: Story
articleTitle: Story
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Story, il tuo strumento essenziale per gestire in modo efficiente gli elementi a livello di blocco come paragrafi e tabelle.
type: docs
weight: 6960
url: /it/net/aspose.words/story/
---
## Story class

Classe base per elementi che contengono nodi a livello di blocco[`Paragraph`](../paragraph/) E[`Table`](../../aspose.words.tables/table/) .

Per saperne di più, visita il[Livelli logici dei nodi in un documento](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) articolo di documentazione.

```csharp
public abstract class Story : CompositeNode
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Ottiene il primo paragrafo della storia. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ottiene il tipo di questo nodo. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ottiene il tipo di questa storia. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ottiene una raccolta di tabelle che sono figlie immediate della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accetta un visitatore. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Quando implementato in una classe derivata, richiama il metodo VisitXXXEnd del visitatore del documento specificato. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Quando implementato in una classe derivata, richiama il metodo VisitXXXStart del visitatore del documento specificato. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Un metodo di scelta rapida che crea un[`Paragraph`](../paragraph/) oggetto con testo facoltativo e lo aggiunge alla fine di questo oggetto. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Elimina tutte le forme dal testo di questa storia. |
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
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Si dice che il testo di un documento Word sia composto da più storie. Il testo principale è memorizzato nella storia del testo principale rappresentata da[`Body`](../body/) , ogni intestazione e piè di pagina viene memorizzato in una storia separata rappresentata da[`HeaderFooter`](../headerfooter/).

## Esempi

Mostra come rimuovere tutte le forme da un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un DocumentBuilder per inserire una forma. Questa è una forma in linea,
// che ha un Paragrafo padre, che è un nodo figlio del Corpo della prima sezione.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Possiamo eliminare tutte le forme dai paragrafi figlio di questo Corpo.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* class [CompositeNode](../compositenode/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
