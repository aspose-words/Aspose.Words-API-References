---
title: SaveSubsetFonts
second_title: Aspose.Words for .NET API Reference
description: FontInfoCollection property. Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is false in C#.
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

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### See Also

* class [FontInfoCollection](../)
* namespace [Aspose.Words.Fonts](../../fontinfocollection/)
* assembly [Aspose.Words](../../../)
