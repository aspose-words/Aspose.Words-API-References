---
title: Interface IStructuredDocumentTag
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Markup.IStructuredDocumentTag interfaccia. Interfaccia per definire dati comuniStructuredDocumentTag EStructuredDocumentTagRangeStart .
type: docs
weight: 3970
url: /it/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interfaccia per definire dati comuni[`StructuredDocumentTag`](../structureddocumenttag/) E[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Ottiene o imposta il colore del tag del documento strutturato. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Specifica un ID numerico persistente univoco di sola lettura per questo **SDT**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Specifica se il contenuto di this **SDT** deve essere interpretato in modo da contenere il segnaposto text (al contrario dei normali contenuti di testo all'interno dell'SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Ottiene il livello al quale this **SDT** si verifica nell'albero del documento. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Se impostata su true, questa proprietà impedirà a un utente di eliminarla **SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Se impostata su true, questa proprietà impedirà a un utente di modificarne il contenuto **SDT** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Ottiene il file[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)contenente testo segnaposto che deve essere visualizzato quando i contenuti dell'esecuzione di questo SDT sono vuoti, l'elemento XML mappato associato è vuoto come specificato tramite[`XmlMapping`](./xmlmapping/) element o il[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'elemento è vero. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Ottiene o imposta il nome di[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Ottiene il tipo di this **Tag documento strutturato** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Specifica un tag associato al nodo SDT corrente. Non può essere null. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Specifica il nome descrittivo associato a questo **SDT** . Non può essere nullo. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc formato. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Ottiene un oggetto che rappresenta la mappatura di questo tag di documento strutturato su dati XML in una parte XML personalizzata del documento corrente. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Restituisce true se questa istanza è un tag di documento strutturato con intervalli. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Restituisce l'oggetto Node che implementa questa interfaccia. |

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)


