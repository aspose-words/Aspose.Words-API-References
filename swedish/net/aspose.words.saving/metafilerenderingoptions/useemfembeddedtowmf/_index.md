---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen UseEmfEmbeddedToWmf optimerar rendering av WMF-metafiler, vilket förbättrar prestanda och kvalitet för dina grafikprogram.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Hämtar eller ställer in ett värde som avgör hur WMF-metafiler med inbäddade EMF-metafiler ska renderas.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Anmärkningar

WMF-metafiler kan innehålla inbäddade EMF-data. MS Word använder i de flesta fall inbäddade EMF-data. GDI+ använder alltid WMF-data.

När detta värde är inställt på`sann`Aspose.Words använder inbäddad EMF-data vid rendering.

När detta värde är inställt på`falsk`Aspose.Words använder WMF-data vid rendering.

Det här alternativet används endast när metafilen renderas som vektorgrafik. När metafilen renderas till bitmapp används alltid WMF-data.

Standardvärdet är`sann`.

## Exempel

Visar hur man konfigurerar renderingsalternativ relaterade till Enhanced Windows Metafile när man sparar till PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.Emf"
// för att endast rendera EMF-delen av en EMF+ dubbelmetafil.
// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlus" för att
// för att rendera EMF+-delen av en EMF+ dubbelmetafil.
// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// för att rendera EMF+-delen av en EMF+ dubbelmetafil om alla EMF+-poster stöds.
// Annars kommer Aspose.Words att rendera EMF-delen.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Sätt egenskapen "UseEmfEmbeddedToWmf" till "true" för att rendera inbäddad EMF-data
// för metafiler som vi kan rendera som vektorgrafik.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
