---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions CacheBackgroundGraphics för att optimera cachelagring av dokumentgrafik, vilket förbättrar din PDF-skapande och prestanda.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Hämtar eller anger ett värde som avgör om grafik som placeras i dokumentets bakgrund ska cachelagras eller inte.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` och bakgrundsgrafik skrivs till PDF-dokumentet som ett xObject.

När värdet är`falsk` Bakgrundsgrafik cachas inte.

Vissa former stöds inte för cachning (former med fält, bokmärken, HRefs).

Dokumentbakgrundsgrafik är olika former, diagram, bilder placerade i sidfoten eller sidhuvudet, samt bakgrund och kantlinje på en sida.

## Exempel

Visar hur man cachar grafik som placeras i dokumentets bakgrund.

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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
