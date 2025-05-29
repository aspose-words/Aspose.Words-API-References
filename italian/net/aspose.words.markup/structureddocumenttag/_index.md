---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Markup.StructuredDocumentTag per un controllo efficiente dei contenuti nei documenti. Migliora la gestione dei tuoi documenti con le funzionalità di SDT!
type: docs
weight: 4750
url: /it/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Rappresenta un tag di documento strutturato (SDT o controllo del contenuto) in un documento.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | Inizializza una nuova istanza di**Tag del documento strutturato** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Ottiene/imposta l'aspetto di un tag di documento strutturato. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Specifica la categoria del blocco di costruzione per questo**SDT** node. Non può essere`null` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Specifica il tipo di blocco di costruzione per questo**SDT** . Non può essere`null` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Specifica il tipo di calendario per questo**SDT** . Il valore predefinito èDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Ottiene/imposta lo stato corrente della casella di controllo**SDT** . Il valore predefinito per questa proprietà è`falso` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Formattazione del carattere che verrà applicata al testo immesso in**SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Stringa che rappresenta il formato in cui vengono visualizzate le date. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Consente di impostare/ottenere il formato della lingua per la data visualizzata in questo**SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Ottiene/imposta il formato in cui viene memorizzata la data per una data SDT quando**SDT** è legato a un nodo XML nell'archivio dati del documento. Il valore predefinito èDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Formattazione del carattere che verrà applicata all'ultimo carattere del testo immesso in**SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Specifica la data e l'ora complete inserite per l'ultima volta in questo**SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Specifica un ID numerico persistente di sola lettura univoco per questo**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Specifica se il contenuto di questo**SDT** deve essere interpretato come contenente testo segnaposto (al contrario dei normali contenuti di testo all'interno dell'SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Specifica se questo**SDT** verrà rimosso dal documento WordProcessingML quando il suo contenuto viene modificato. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Ottiene il livello a cui questo**SDT** si verifica nell'albero del documento. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Ottiene[`SdtListItemCollection`](../sdtlistitemcollection/) associato a questo**SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | Quando impostato su`VERO` , questa proprietà impedirà a un utente di eliminare questo**SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | Quando impostato su`VERO` , questa proprietà impedirà a un utente di modificare il contenuto di questo**SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Specifica se questo**SDT** consente più righe di testo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | RestituisceStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Ottiene il[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto che dovrebbe essere visualizzato quando il contenuto di questa esecuzione SDT è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping/) elemento o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'elemento è`VERO` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Ottiene o imposta il nome del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Ottiene il tipo di questo**Tag del documento strutturato** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Ottiene o imposta lo stile del tag del documento strutturato. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Ottiene o imposta il nome dello stile applicato al tag del documento strutturato. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Specifica un tag associato al nodo SDT corrente. Non può essere`null` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Specifica il nome descrittivo associato a questo**SDT** . Non può essere`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc formato. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc format. A differenza del[`WordOpenXML`](./wordopenxml/) proprietà, questo metodo genera un documento ridotto che esclude tutte le parti non correlate al contenuto. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato la fine dello StructuredDocumentTag. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio dello StructuredDocumentTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Cancella il contenuto di questo tag di documento strutturato e visualizza un segnaposto se definito. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
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
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Rimuove solo questo nodo SDT, ma ne mantiene il contenuto all'interno dell'albero del documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | Imposta il simbolo utilizzato per rappresentare lo stato selezionato di un controllo del contenuto della casella di controllo. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | Imposta il simbolo utilizzato per rappresentare lo stato non selezionato di un controllo del contenuto di una casella di controllo. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

I tag di documento strutturato (SDT) consentono di incorporare la semantica definita dal cliente, nonché il suo comportamento e aspetto, in un documento.

In questa versione Aspose.Words fornisce una serie di metodi e proprietà pubbliche per manipolare il comportamento e il contenuto di`StructuredDocumentTag` . La mappatura dei nodi SDT su pacchetti XML personalizzati all'interno di un documento può essere eseguita utilizzando [`XmlMapping`](./xmlmapping/) proprietà.

`StructuredDocumentTag` può verificarsi in un documento nei seguenti punti:

* A livello di blocco - Tra paragrafi e tabelle, come figlio di un[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) o un[`Shape`](../../aspose.words.drawing/shape/) nodo.
* Livello di riga - Tra le righe di una tabella, come figlio di una[`Table`](../../aspose.words.tables/table/) nodo.
* A livello di cella - Tra le celle in una riga di tabella, come figlio di una[`Row`](../../aspose.words.tables/row/) nodo.
* Livello in linea - Tra i contenuti in linea all'interno, come figlio di un[`Paragraph`](../../aspose.words/paragraph/).
* Annidato dentro un altro`StructuredDocumentTag`.

## Esempi

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto stile dalla raccolta stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Riferimento a uno stile nel documento tramite il nome:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Guarda anche

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
