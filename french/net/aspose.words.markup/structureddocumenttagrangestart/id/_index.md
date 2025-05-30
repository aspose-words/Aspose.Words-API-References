---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StructuredDocumentTagRangeStart Id  votre clé vers un identifiant numérique unique en lecture seule pour un balisage efficace des documents.
type: docs
weight: 40
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Spécifie un identifiant numérique persistant unique en lecture seule pour cette balise de document structuré.

```csharp
public int Id { get; }
```

## Remarques

L'attribut Id doit suivre ces règles :

* Le document ne conservera les identifiants de balises de document structurés que si l'ensemble du document est cloné[`Clone`](../../../aspose.words/document/clone/).
* Pendant[`ImportNode`](../../../aspose.words/documentbase/importnode/) L'ID doit être conservé si l'importation ne provoque pas de conflits avec d'autres ID de balises de document structuré dans le document cible.
* Si plusieurs nœuds de balises de document structuré spécifient la même valeur de nombre décimal pour l'attribut Id, , alors la première balise de document structuré dans le document doit conserver cet Id d'origine, et tous les nœuds de balises de document structuré suivants doivent se voir attribuer de nouveaux identifiants lors du chargement du document.
* Pendant la balise de document structuré autonomeINodeCloningListener) l'opération un nouvel ID unique sera généré pour le nœud de balise de document structuré cloné.
* Si l'identifiant n'est pas spécifié dans le document source, le nœud de balise de document structuré doit avoir un nouvel identifiant unique qui lui est attribué lorsque le document est chargé.

## Exemples

Montre comment obtenir les propriétés des balises de document structurées à plusieurs sections.

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

### Voir également

* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
