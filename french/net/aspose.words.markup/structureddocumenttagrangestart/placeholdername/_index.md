---
title: StructuredDocumentTagRangeStart.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer la propriété PlaceholderName pour StructuredDocumentTagRangeStart, améliorant ainsi l'efficacité des blocs de construction de votre document.
type: docs
weight: 120
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/placeholdername/
---
## StructuredDocumentTagRangeStart.PlaceholderName property

Obtient ou définit le nom du[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé.

```csharp
public string PlaceholderName { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Lancer si BuildingBlock avec ce nom[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) n'est pas présent dans[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/). |

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
