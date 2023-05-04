---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words for .NET
description: FontInfoCollection EmbedTrueTypeFonts property. Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is false in C#.
type: docs
weight: 30
url: /net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is `false`.

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Remarks

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

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
