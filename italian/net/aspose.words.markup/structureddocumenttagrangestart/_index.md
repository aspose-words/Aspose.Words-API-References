---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Markup.StructuredDocumentTagRangeStart, che consente una gestione fluida dei contenuti multisezione nei documenti strutturati.
type: docs
weight: 4780
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Rappresenta un inizio di**a distanza** tag di documento strutturato che accetta contenuti multi-sezione. Vedi anche[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Inizializza una nuova istanza di**Inizio intervallo tag documento strutturato** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | Ottiene o imposta l'aspetto del tag del documento strutturato. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Specifica un ID numerico persistente e di sola lettura univoco per questo tag di documento strutturato. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Specifica se il contenuto di questo tag del documento strutturato deve essere interpretato come contenente testo segnaposto (in contrapposizione al normale contenuto di testo all'interno del tag del documento strutturato). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Ottiene l'ultimo elemento figlio nell'intervallo stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Ottiene il livello in cui si verifica l'inizio dell'intervallo di tag di questo documento strutturato nell'albero del documento. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Quando impostato su`VERO` , questa proprietà impedirà a un utente di eliminare questo tag di documento strutturato. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Quando impostato su`VERO` , questa proprietà impedirà a un utente di modificare il contenuto di questo tag di documento strutturato. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | RestituisceStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Ottiene il[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)contenente testo segnaposto che dovrebbe essere visualizzato quando il contenuto di esecuzione del tag di questo documento strutturato è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping/) elemento o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'elemento è`VERO` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Ottiene o imposta il nome del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Specifica la fine dell'intervallo se[`StructuredDocumentTag`](../structureddocumenttag/) è un tag di documento strutturato con intervallo. Altrimenti restituisce`null` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Ottiene il tipo di questo tag di documento strutturato. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Specifica un tag associato al nodo tag del documento strutturato corrente. Non può essere`null` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Specifica il nome descrittivo associato a questo tag di documento strutturato. Non può essere`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc formato. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc format. A differenza del[`WordOpenXML`](./wordopenxml/) proprietà, questo metodo genera un documento ridotto che esclude tutte le parti non correlate al contenuto. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Ottiene un oggetto che rappresenta la mappatura di questo intervallo di tag di documenti strutturati ai dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Aggiunge il nodo specificato alla fine dell'intervallo stdContent. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono ai tipi specificati. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Rimuove tutti i nodi tra questo nodo di inizio intervallo e il nodo di fine intervallo. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Rimuove questo inizio intervallo e i nodi di fine intervallo appropriati del tag del documento strutturato, ma mantiene il suo contenuto all'interno dell'albero del documento. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Può essere figlio immediato di[`Body`](../../aspose.words/body/) nodo**soltanto** .

## Esempi

Mostra come ottenere le proprietà dei tag dei documenti strutturati multisezione.

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

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
