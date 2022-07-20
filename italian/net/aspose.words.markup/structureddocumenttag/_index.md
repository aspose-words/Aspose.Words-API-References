---
title: StructuredDocumentTag
second_title: Aspose.Words per .NET API Reference
description: Rappresenta un tag di documento strutturato SDT o controllo del contenuto in un documento.
type: docs
weight: 3820
url: /it/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Rappresenta un tag di documento strutturato (SDT o controllo del contenuto) in un documento.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | Inizializza una nuova istanza di **Tag del documento strutturato** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | Ottiene/imposta l'aspetto di un tag di documento strutturato. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | Specifica la categoria del building block per questo **SDT** node. Non può essere null. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | Specifica il tipo di building block per questo **SDT** . Non può essere nullo. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | Specifica il tipo di calendario per questo **SDT** . L'impostazione predefinita èDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | Ottiene/imposta lo stato corrente della casella di controllo **SDT** . Il valore predefinito per questa proprietà è false. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ottiene tutti i nodi figlio immediati di questo nodo. |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | Formattazione del carattere che verrà applicata al testo inserito **SDT** . |
| [Count](../../aspose.words/compositenode/count) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | Stringa che rappresenta il formato in cui vengono visualizzate le date. Non può essere null. Le date per l'inglese (Stati Uniti) sono "mm/gg/aaaa" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | Consente di impostare/ottenere il formato della lingua per la data visualizzata in questo **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | Ottiene/imposta il formato in cui viene archiviata la data per un SDT di data quando il **SDT** è associato a un nodo XML nell'archivio dati del documento. Il valore predefinito èDateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | Formattazione del carattere che verrà applicata all'ultimo carattere del testo inserito **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ottiene il primo figlio del nodo. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | Specifica la data e l'ora complete immesse per l'ultima volta **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Restituisce true se questo nodo ha nodi figlio. |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | Specifica un ID numerico persistente di sola lettura univoco per questo **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Restituisce true poiché questo nodo può avere nodi figlio. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | Specifica se il contenuto di questo **SDT** deve essere interpretato per contenere testo segnaposto (al contrario dei normali contenuti di testo all'interno dell'SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | Specifica se questo **SDT** deve essere rimosso dal documento WordProcessingML quando il suo contenuto viene modificato. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ottiene l'ultimo figlio del nodo. |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | Ottiene il livello a cui questo **SDT** si verifica nell'albero dei documenti. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | Ottiene[`SdtListItemCollection`](../sdtlistitemcollection) associato a questo **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | Se impostata su true, questa proprietà vieterà a un utente di eliminarlo **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | Se impostata su true, questa proprietà vieterà a un utente di modificarne il contenuto **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | Specifica se questo **SDT** consente più righe di testo. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | Restituisce **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | Ottiene il[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) contenente testo segnaposto che dovrebbe essere visualizzato quando il contenuto di questa esecuzione SDT è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping) element o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext) elemento è vero. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | Ottiene o imposta il nome del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) contenente testo segnaposto. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | Ottiene il tipo di questo **Tag del documento strutturato** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | Ottiene o imposta lo stile del tag del documento strutturato. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | Ottiene o imposta il nome dello stile applicato al tag del documento strutturato. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | Specifica un tag associato al nodo SDT corrente. Non può essere null. |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | Specifica il nome descrittivo associato a questo **SDT** . Non può essere nullo. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | Ottiene una stringa che rappresenta l'XML contenuto all'interno del nodo nel fileFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | Ottiene un oggetto che rappresenta il mapping di questo tag del documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | Cancella il contenuto di questo tag del documento strutturato e visualizza un segnaposto se è definito. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Riservato per l'uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Restituisce un ennesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Restituisce l'indice del nodo figlio specificato nell'array del nodo figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Rimuove il nodo figlio specificato. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | Rimuove solo questo nodo SDT stesso, ma ne mantiene il contenuto all'interno dell'albero del documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Rimuove tutto[`SmartTag`](../smarttag) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Seleziona il primo nodo che corrisponde all'espressione XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | Imposta il simbolo utilizzato per rappresentare lo stato selezionato di un controllo del contenuto di una casella di controllo. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | Imposta il simbolo utilizzato per rappresentare lo stato deselezionato di un controllo del contenuto di una casella di controllo. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

I tag di documento strutturati (SDT) consentono di incorporare la semantica definita dal cliente, nonché il suo comportamento e aspetto in un documento.

In questa versione Aspose.Words fornisce una serie di metodi e proprietà pubblici per manipolare il comportamento e il contenuto di[`StructuredDocumentTag`](../structureddocumenttag) . È possibile eseguire la mappatura di nodi SDT su pacchetti XML personalizzati all'interno di un documento utilizzando [`XmlMapping`](./xmlmapping) proprietà.

[`StructuredDocumentTag`](../structureddocumenttag) può verificarsi in un documento nei seguenti luoghi:

* Block-level - Tra paragrafi e tabelle, da figlio di a[`Body`](../../aspose.words/body) ,[`HeaderFooter`](../../aspose.words/headerfooter) , [`Comment`](../../aspose.words/comment) ,[`Footnote`](../../aspose.words.notes/footnote) o a[`Shape`](../../aspose.words.drawing/shape) nodo.
* A livello di riga: tra le righe di una tabella, come figlio di a[`Table`](../../aspose.words.tables/table) nodo.
* A livello di cella: tra le celle in una riga di tabella, come figlio di a[`Row`](../../aspose.words.tables/row) nodo.
* Inline-level - Tra i contenuti inline all'interno, da figlio di a[`Paragraph`](../../aspose.words/paragraph).
* Nidificato dentro un altro[`StructuredDocumentTag`](../structureddocumenttag).

### Esempi

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto di stile dalla raccolta di stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Fai riferimento a uno stile nel documento per nome:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Guarda anche

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
