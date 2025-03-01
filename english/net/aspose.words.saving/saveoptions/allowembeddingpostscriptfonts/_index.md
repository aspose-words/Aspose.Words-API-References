---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words for .NET
description: Control font embedding in your documents with SaveOptions' AllowEmbeddingPostScriptFonts. Easily manage TrueType font options for enhanced document quality.
type: docs
weight: 20
url: /net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is `false`.

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Remarks

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) of the [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) property is set to `true`.

## Examples

Shows how to save the document with PostScript font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Load the font with PostScript to use in the document.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Embed TrueType fonts.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Allow embedding PostScript fonts while embedding TrueType fonts.
// Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
