---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words för .NET
description: Styr inbäddning av teckensnitt i dina dokument med SaveOptions AllowEmbeddingPostScriptFonts. Hantera enkelt alternativ för TrueType-teckensnitt för förbättrad dokumentkvalitet.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Anmärkningar

Observera att Word inte bäddar in PostScript-teckensnitt, men kan öppna dokument med inbäddade teckensnitt av den här typen.

Det här alternativet fungerar bara när[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) av [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) egendomen är inställd på`sann`.

## Exempel

Visar hur man sparar dokumentet med PostScript-teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Laddar typsnittet med PostScript som ska användas i dokumentet.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Bädda in TrueType-teckensnitt.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Tillåt inbäddning av PostScript-teckensnitt samtidigt som TrueType-teckensnitt bäddas in.
// Microsoft Word bäddar inte in PostScript-teckensnitt, men kan öppna dokument med inbäddade teckensnitt av den här typen.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
