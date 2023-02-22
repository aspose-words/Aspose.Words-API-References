---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Aspose.Words för .NET API Referens
description: MetafileRenderingOptions fast egendom. Hämtar eller ställer in ett värde som bestämmer hur EMF Dualmetafiler ska renderas.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Hämtar eller ställer in ett värde som bestämmer hur EMF+ Dual-metafiler ska renderas.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### Anmärkningar

EMF+ Dual metafiler innehåller både EMF+ och EMF delar. MS Word och GDI+ renderar alltid EMF+-delen. Aspose.Words stöder för närvarande inte alla EMF+-poster fullt ut och i vissa fall ser renderingsresultatet av EMF-delen bättre ut än renderingsresultatet av EMF+-delen.

Det här alternativet används endast när metafilen renderas som vektorgrafik. När metafil renderas till bitmapp används alltid EMF+-delen.

Standardvärdet ärEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../metafilerenderingoptions/)
* hopsättning [Aspose.Words](../../../)


