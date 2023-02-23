---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
second_title: Aspose.Words for .NET API Reference
description: FontInfoCollection property. Specifies whether or not to embed System fonts into the document. Default value for this property is false in C#.
type: docs
weight: 20
url: /net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Specifies whether or not to embed System fonts into the document. Default value for this property is `false`.

This option works only when [`EmbedTrueTypeFonts`](../embedtruetypefonts/) option is set to `true`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Remarks

Setting this property to `true` is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

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
