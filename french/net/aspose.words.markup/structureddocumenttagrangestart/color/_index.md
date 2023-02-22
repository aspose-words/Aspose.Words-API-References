---
title: StructuredDocumentTagRangeStart.Color
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTagRangeStart propriété. Obtient ou définit la couleur de la balise de document structuré.
type: docs
weight: 30
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/color/
---
## StructuredDocumentTagRangeStart.Color property

Obtient ou définit la couleur de la balise de document structuré.

```csharp
public Color Color { get; set; }
```

### Exemples

Montre comment obtenir les propriétés des balises de document structuré à plusieurs sections.

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
* espace de noms [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* Assemblée [Aspose.Words](../../../)


