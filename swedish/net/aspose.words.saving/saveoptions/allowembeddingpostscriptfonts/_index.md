---
title: SaveOptions.AllowEmbeddingPostScriptFonts
second_title: Aspose.Words för .NET API Referens
description: SaveOptions fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueTypeteckensnitt i ett dokument på det sparas. Standardvärdet är falsk .
type: docs
weight: 20
url: /sv/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

### Anmärkningar

Obs, Word bäddar inte in PostScript-teckensnitt, men kan öppna dokument med inbäddade typsnitt av denna typ.

Det här alternativet fungerar bara när[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) av [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) egenskapen är inställd på`Sann`.

### Exempel

Visar hur du sparar dokumentet med PostScript-teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Ladda teckensnittet med PostScript för att använda i dokumentet.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Bädda in TrueType-teckensnitt.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Tillåt inbäddning av PostScript-teckensnitt medan TrueType-teckensnitt bäddas in.
// Microsoft Word bäddar inte in PostScript-teckensnitt, men kan öppna dokument med inbäddade typsnitt av denna typ.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../saveoptions/)
* hopsättning [Aspose.Words](../../../)


