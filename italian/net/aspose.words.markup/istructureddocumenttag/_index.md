---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words per .NET
description: Esplora l'interfaccia Aspose.Words.Markup.IStructuredDocumentTag per una gestione efficiente dei tag dei documenti strutturati e migliora subito l'elaborazione dei tuoi documenti!
type: docs
weight: 4660
url: /it/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interfaccia per definire un dato comune per[`StructuredDocumentTag`](../structureddocumenttag/) E[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Ottiene o imposta l'aspetto del tag del documento strutturato. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Specifica un ID numerico persistente di sola lettura univoco per questo**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Restituisce true se questa istanza è un tag di documento strutturato con intervallo (multi-sezione). |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Specifica se il contenuto di questo**SDT** deve essere interpretato come contenente testo segnaposto (al contrario dei normali contenuti di testo all'interno dell'SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Ottiene il livello a cui questo**SDT** si verifica nell'albero del documento. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Se impostato su true, questa proprietà impedirà a un utente di eliminare questo**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Se impostata su true, questa proprietà impedirà a un utente di modificare il contenuto di questo**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Restituisce l'oggetto Node che implementa questa interfaccia. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Ottiene il[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto che dovrebbe essere visualizzato quando il contenuto di questa esecuzione SDT è vuoto, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping/) elemento o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'elemento è vero. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Ottiene o imposta il nome del[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Ottiene il tipo di questo**Tag del documento strutturato** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Specifica un tag associato al nodo SDT corrente. Non può essere nullo. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Specifica il nome descrittivo associato a questo**SDT** . Non può essere nullo. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono ai tipi specificati. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Rimuove solo questo nodo SDT, ma ne mantiene il contenuto all'interno dell'albero del documento. |

## Esempi

Mostra come rimuovere il tag del documento strutturato, mantenendone però il contenuto al suo interno.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Questa raccolta fornisce un'interfaccia unificata per accedere ai tag strutturati con e senza intervallo.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Qui possiamo ottenere i nodi figlio dall'interfaccia comune dei tag strutturati con e senza intervallo.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
