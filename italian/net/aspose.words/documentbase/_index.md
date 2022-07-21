---
title: DocumentBase
second_title: Aspose.Words per .NET API Reference
description: Fornisce la classe base astratta per un documento principale e un documento di glossario di un documento Word.
type: docs
weight: 430
url: /it/net/aspose.words/documentbase/
---
## DocumentBase class

Fornisce la classe base astratta per un documento principale e un documento di glossario di un documento Word.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Ottiene o imposta la forma dello sfondo del documento. Può essere nullo. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ottiene tutti i nodi figlio immediati di questo nodo. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ottiene il primo figlio del nodo. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Restituisce true se questo nodo ha nodi figlio. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Restituisce true poiché questo nodo può avere nodi figlio. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ottiene l'ultimo figlio del nodo. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Fornisce l'accesso alla formattazione dell'elenco utilizzata nel documento. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Ottiene il tipo di questo nodo. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione più semplice di[`BackgroundShape`](./backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Consente di controllare come vengono caricate le risorse esterne. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Restituisce una raccolta di stili definiti nel documento. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare una perdita di fedeltà dei dati o della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Riservato per l'uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Restituisce un ennesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode)(Node, bool) | Importa un nodo da un altro documento nel documento corrente. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode_1)(Node, bool, ImportFormatMode) | Importa un nodo da un altro documento nel documento corrente con un'opzione per controllare la formattazione. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Restituisce l'indice del nodo figlio specificato nell'array del nodo figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Seleziona il primo nodo che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Aspose.Words rappresenta un documento di Word come un albero di nodi.[`DocumentBase`](../documentbase) è un nodo radice dell'albero che contiene tutti gli altri nodi del documento.

[`DocumentBase`](../documentbase) memorizza anche informazioni a livello di documento come[`Styles`](./styles) e [`Lists`](./lists) a cui i nodi dell'albero potrebbero fare riferimento.

### Esempi

Mostra come inizializzare le sottoclassi di DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Guarda anche

* class [CompositeNode](../compositenode)
* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
