---
title: Class Story
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Story classe. Classe base per elementi che contengono nodi a livello di bloccoParagraph ETable .
type: docs
weight: 6110
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
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Ottiene l'ultimo paragrafo della storia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ottiene il tipo di questo nodo. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Ottiene una raccolta di paragrafi che sono figli immediati della storia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Ottiene il tipo di questa storia. |
| [Tables](../../aspose.words/story/tables/) { get; } | Ottiene una raccolta di tabelle che sono figli immediati della storia. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accetta un visitatore. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(DocumentVisitor) |  |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | Un metodo di scelta rapida che crea un file[`Paragraph`](../paragraph/) oggetto con testo facoltativo e lo aggiunge alla fine di questo oggetto. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Elimina tutte le forme dal testo di questa storia. |
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
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Si dice che il testo di un documento Word sia costituito da più brani. Il testo principale è memorizzato nel brano di testo principale rappresentato da[`Body`](../body/) , ciascuna intestazione e piè di pagina vengono archiviati in una storia separata rappresentata da[`HeaderFooter`](../headerfooter/).

### Esempi

Mostra come rimuovere tutte le forme da un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un DocumentBuilder per inserire una forma. Questa è una forma in linea,
// che ha un Paragrafo genitore, che è un nodo figlio del Corpo della prima sezione.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Possiamo eliminare tutte le forme dai paragrafi figlio di questo Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* class [CompositeNode](../compositenode/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


