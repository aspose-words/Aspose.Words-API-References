---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words for .NET
description: Discover the FontInfoCollection SaveSubsetFonts property, control embedded TrueType font subsets in your documents for optimized file size and performance.
type: docs
weight: 50
url: /net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is `false`.

This option works only when [`EmbedTrueTypeFonts`](../embedtruetypefonts/) property is set to `true`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Remarks

This option works for DOC, DOCX and RTF formats only.

## Examples

Shows how to save a document with embedded TrueType fonts.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### See Also

* class [FontInfoCollection](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
