---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen EmfPlusDualRenderingMode förbättrar EMF Dual-metafilrendering. Optimera din grafik med flexibla renderingsalternativ idag!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Hämtar eller ställer in ett värde som avgör hur EMF+ Dual-metafiler ska renderas.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Anmärkningar

EMF+ Dual-metafiler innehåller både EMF+- och EMF-delar. MS Word och GDI+ renderar alltid EMF+-delen. Aspose.Words stöder för närvarande inte alla EMF+-poster fullt ut och i vissa fall ser renderingen av resultatet av EMF-delen bättre ut än renderingen av resultatet av EMF+-delen.

Det här alternativet används endast när metafilen renderas som vektorgrafik. När metafilen renderas till bitmapp används alltid EMF+-delen.

Standardvärdet ärEmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
