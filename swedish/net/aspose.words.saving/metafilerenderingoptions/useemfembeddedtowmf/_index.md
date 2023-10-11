---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
second_title: Aspose.Words för .NET API Referens
description: MetafileRenderingOptions fast egendom. Hämtar eller ställer in ett värde som bestämmer hur WMFmetafiler med inbäddade EMFmetafiler ska renderas.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Hämtar eller ställer in ett värde som bestämmer hur WMF-metafiler med inbäddade EMF-metafiler ska renderas.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

### Anmärkningar

WMF-metafiler kan innehålla inbäddade EMF-data. MS Word använder i de flesta fall inbäddade EMF-data. GDI+ använder alltid WMF-data.

När detta värde är satt till`Sann`, Aspose.Words använder inbäddade EMF-data vid rendering.

När detta värde är satt till`falsk`, Aspose.Words använder WMF-data vid rendering.

Det här alternativet används endast när metafilen renderas som vektorgrafik. När metafil renderas till bitmapp används alltid WMF-data.

Standardvärdet är`Sann`.

### Exempel

Visar hur du konfigurerar förbättrade Windows Metafil-relaterade renderingsalternativ när du sparar till PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.Emf"
// för att endast återge EMF-delen av en EMF+ dubbel metafil.
// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlus" till
// för att återge EMF+ delen av en EMF+ dubbel metafil.
// Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// för att återge EMF+-delen av en EMF+ dubbel metafil om alla EMF+-poster stöds.
// Annars kommer Aspose.Words att återge EMF-delen.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Ställ in egenskapen "UseEmfEmbeddedToWmf" till "true" för att återge inbäddade EMF-data
// för metafiler som vi kan rendera som vektorgrafik.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../metafilerenderingoptions/)
* hopsättning [Aspose.Words](../../../)


