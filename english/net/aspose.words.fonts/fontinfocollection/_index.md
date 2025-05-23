---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fonts.FontInfoCollection class, your go-to solution for managing document fonts efficiently and enhancing your document's visual appeal.
type: docs
weight: 3360
url: /net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Represents a collection of fonts used in a document.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Specifies whether or not to embed System fonts into the document. Default value for this property is `false`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is `false`. |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Gets a font with the specified name. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is `false`. |

## Methods

| Name | Description |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Determines whether the collection contains a font with the given name. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |

## Remarks

Items are [`FontInfo`](../fontinfo/) objects.

You do not create instances of this class directly. Use the [`FontInfos`](../../aspose.words/documentbase/fontinfos/) property to access the collection of fonts defined in the document.

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

Shows how to print the details of what fonts are present in a document.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Print all the used and unused fonts in the document.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### See Also

* class [FontInfo](../fontinfo/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
