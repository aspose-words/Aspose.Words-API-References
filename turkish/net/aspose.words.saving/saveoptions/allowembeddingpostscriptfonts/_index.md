---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words for .NET
description: SaveOptions AllowEmbeddingPostScriptFonts mülk. Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Kaydedildikten sonra TrueType yazı tiplerini bir belgeye gömerken PostScript ana hatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Notlar

Word'ün PostScript yazı tiplerini katıştırmadığını ancak bu türden katıştırılmış yazı tiplerine sahip belgeleri açabileceğini unutmayın.

Bu seçenek yalnızca şu durumlarda çalışır:[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) of the [`FontInfos`](../../../aspose.words/documentbase/fontinfos/) özellik şu şekilde ayarlandı:`doğru`.

## Örnekler

Belgenin PostScript yazı tipiyle nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Belgede kullanılacak yazı tipini PostScript ile yükleyin.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// TrueType yazı tiplerini gömün.
doc.FontInfos.EmbedTrueTypeFonts = true;

// TrueType yazı tiplerini gömerken PostScript yazı tiplerinin de gömülmesine izin ver.
// Microsoft Word, PostScript yazı tiplerini gömmez ancak bu türden gömülü yazı tiplerine sahip belgeleri açabilir.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
