---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.EmfPlusDualRenderingMode uppräkning. Anger hur Aspose.Words ska återge EMF Dual metafiler i C#.
type: docs
weight: 4980
url: /sv/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Anger hur Aspose.Words ska återge EMF+ Dual metafiler.

```csharp
public enum EmfPlusDualRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words försöker göra EMF+ till en del av EMF+ Dual metafil. Om några av EMF+-posterna inte stöds så återger Aspose.Words EMF till en del av EMF+ Dual metafil. |
| EmfPlus | `1` | Aspose.Words återger EMF+ till en del av EMF+ Dual metafil. |
| Emf | `2` | Aspose.Words återger EMF till en del av EMF+ Dual metafil. |

## Exempel

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
