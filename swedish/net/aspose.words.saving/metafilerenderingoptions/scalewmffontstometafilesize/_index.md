---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Aspose.Words för .NET API Referens
description: MetafileRenderingOptions fast egendom. Hämtar eller ställer in ett värde som avgör om teckensnitt ska skalas eller inte i WMFmetafil enligt metafilstorlek på sidan.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Hämtar eller ställer in ett värde som avgör om teckensnitt ska skalas eller inte i WMF-metafil enligt metafilstorlek på sidan.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Anmärkningar

När WMF-metafiler visas i MS Word, kan teckensnitt skalas enligt den faktiska metafilstorleken på sidan.

När detta värde är satt till`Sann`, Aspose.Words emulerar teckensnittsskalning enligt metafilstorlek på sidan.

När detta värde är satt till`falsk`, Aspose.Words visar typsnitten när metafilen renderas till sin standardstorlek.

Det här alternativet används endast när metafilen renderas som vektorgrafik.

Standardvärdet är`Sann`.

### Exempel

Visar hur WMF-teckensnitt skalas efter metafilstorlek på sidan.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "ScaleWmfFontsToMetafileSize" till "true" för att skala teckensnitt
// som formaterar text i WMF-bilder enligt storleken på metafilen på sidan.
// Ställ in egenskapen "ScaleWmfFontsToMetafileSize" till "false" till
// bevara standardskalan för dessa teckensnitt.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../metafilerenderingoptions/)
* hopsättning [Aspose.Words](../../../)


