---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTagRangeStart Id la chiave per un identificatore numerico univoco e di sola lettura per un tagging efficiente dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Specifica un ID numerico persistente e di sola lettura univoco per questo tag di documento strutturato.

```csharp
public int Id { get; }
```

## Osservazioni

L'attributo Id deve seguire queste regole:

* Il documento deve conservare gli ID dei tag del documento strutturato solo se l'intero document viene clonato[`Clone`](../../../aspose.words/document/clone/).
* Durante[`ImportNode`](../../../aspose.words/documentbase/importnode/) L'ID verrà mantenuto se l'importazione non causa conflitti con altri ID tag di documenti strutturati nel documento di destinazione.
* Se più nodi tag di documenti strutturati specificano lo stesso valore numerico decimale per l'attributo Id, , il primo nodo tag di documenti strutturati nel documento deve mantenere questo Id originale, e a tutti i nodi tag di documenti strutturati successivi devono essere assegnati nuovi identificatori quando il documento viene caricato.
* Durante il tag del documento strutturato autonomoINodeCloningListener) operazione verrà generato un nuovo ID univoco be per il nodo tag del documento strutturato clonato.
* Se l'ID non è specificato nel documento sorgente, al nodo tag del documento strutturato verrà assegnato un nuovo identificatore univoco quando il documento viene caricato.

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

* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
