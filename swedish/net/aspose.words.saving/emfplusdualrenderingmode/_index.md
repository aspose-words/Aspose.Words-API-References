---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words EMF Plus Dual Rendering Mode-enum för optimal EMF Dual-metafilrendering. Förbättra din dokumentbehandling med precision!
type: docs
weight: 5730
url: /sv/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Anger hur Aspose.Words ska rendera EMF+ Dual-metafiler.

```csharp
public enum EmfPlusDualRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words försöker rendera EMF+-delen av EMF+ Dual-metafilen. Om vissa av EMF+-posterna inte stöds, renderar Aspose.Words EMF-delen av EMF+ Dual-metafilen. |
| EmfPlus | `1` | Aspose.Words återger EMF+ som en del av EMF+ Dual-metafil. |
| Emf | `2` | Aspose.Words återger EMF-delen av EMF+ Dual-metafil. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
