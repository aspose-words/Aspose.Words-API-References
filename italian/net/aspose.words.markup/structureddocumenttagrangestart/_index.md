---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words per .NET API Reference
description: Rappresenta un inizio di a distanza tag del documento strutturato che accetta contenuti a più sezioni. Vedi ancheStructuredDocumentTagRangeEnd./structureddocumenttagrangeend .
type: docs
weight: 3850
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Rappresenta un inizio di **a distanza** tag del documento strutturato che accetta contenuti a più sezioni. Vedi anche[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart)(DocumentBase, SdtType) | Inizializza una nuova istanza di **Inizio dell'intervallo di tag del documento strutturato** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes) { get; } | Ottiene tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dell'intervallo. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id) { get; } | Specifica un ID numerico persistente di sola lettura univoco per questo tag del documento strutturato. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Restituisce vero se questo nodo può contenere altri nodi. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext) { get; set; } | Specifica se il contenuto di questo tag del documento strutturato deve essere interpretato in modo da contenere testo segnaposto (al contrario dei normali contenuti di testo all'interno del tag del documento strutturato). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild) { get; } | Ottiene l'ultimo figlio nell'intervallo stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level) { get; } | Ottiene il livello in cui questo intervallo di tag del documento strutturato inizia nell'albero del documento. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol) { get; set; } | Se impostata su true, questa proprietà vieterà a un utente di eliminare questo tag del documento strutturato. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents) { get; set; } | Se impostata su true, questa proprietà vieterà a un utente di modificare il contenuto di questo tag del documento strutturato. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder) { get; } | Ottiene il[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) contenente un testo segnaposto che dovrebbe essere visualizzato quando questo tag di documento strutturato esegue il contenuto è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping) elemento o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext) elemento è vero. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername) { get; set; } | Ottiene o imposta il nome del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) contenente testo segnaposto. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend) { get; } | Specifica la fine dell'intervallo se StructuredDocumentTag è un tag di documento strutturato con intervalli. Altrimenti restituisce null. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype) { get; } | Ottiene il tipo di questo tag del documento strutturato. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag) { get; set; } | Specifica un tag associato al nodo tag del documento strutturato corrente. Non può essere null. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title) { get; set; } | Specifica il nome descrittivo associato a questo tag di documento strutturato. Non può essere null. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml) { get; } | Ottiene una stringa che rappresenta l'XML contenuto all'interno del nodo nel fileFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping) { get; } | Ottiene un oggetto che rappresenta il mapping di questo intervallo di tag del documento strutturato a dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild)(Node) | Aggiunge il nodo specificato alla fine dell'intervallo stdContent. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono ai tipi specificati. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren)() | Rimuove tutti i nodi tra il nodo iniziale di questo intervallo e il nodo finale dell'intervallo. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly)() | Rimuove questo intervallo iniziale e i nodi finali dell'intervallo appropriato del tag del documento strutturato, ma ne mantiene il contenuto all'interno dell'albero del documento. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

Può essere figlio immediato di[`Body`](../../aspose.words/body) nodo **solo** .

### Esempi

Mostra come ottenere le proprietà dei tag di documenti strutturati a più sezioni.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Guarda anche

* class [Node](../../aspose.words/node)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
