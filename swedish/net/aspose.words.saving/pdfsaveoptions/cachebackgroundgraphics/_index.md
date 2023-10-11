---
title: PdfSaveOptions.CacheBackgroundGraphics
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör om grafik placerad i dokumentets bakgrund ska cachelagras eller inte.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Hämtar eller ställer in ett värde som avgör om grafik placerad i dokumentets bakgrund ska cachelagras eller inte.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

### Anmärkningar

Standardvärdet är`Sann` och bakgrundsgrafik skrivs till PDF-dokumentet som ett xObject.

När värdet är`falsk` bakgrundsgrafik cachelagras inte.

Vissa former stöds inte för cachning (former med fält, bokmärken, HRefs).

Dokumentbakgrundsgrafik är olika former, diagram, bilder placerade i sidfoten eller sidhuvudet, samt bakgrund och kant på en sida.

### Exempel

Visar hur man cachelagrar grafik placerad i dokumentets bakgrund.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


