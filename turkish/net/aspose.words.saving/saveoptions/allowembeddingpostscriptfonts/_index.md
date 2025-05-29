---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: .NET için Aspose.Words
description: SaveOptions' AllowEmbeddingPostScriptFonts ile belgelerinize font yerleştirmeyi kontrol edin. Gelişmiş belge kalitesi için TrueType font seçeneklerini kolayca yönetin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

PostScript anahatlarıyla yazı tiplerinin gömülmesine izin verilip verilmeyeceğini belirten bir Boole değeri alır veya ayarlar. Bir belge kaydedildiğinde TrueType yazı tiplerini gömerken. Varsayılan değer`YANLIŞ` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Notlar

Word'ün PostScript yazı tiplerini gömmediğini, ancak bu tür yazı tiplerinin gömüldüğü belgeleri açabileceğini unutmayın.

Bu seçenek yalnızca şu durumlarda işe yarar:[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) x000d'nin_[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) mülk ayarlandı`doğru`.

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

// TrueType yazı tiplerini göm.
doc.FontInfos.EmbedTrueTypeFonts = true;

// TrueType yazı tiplerini gömerken PostScript yazı tiplerini gömmeye izin ver.
// Microsoft Word, PostScript yazı tiplerini gömmez, ancak bu tür yazı tiplerinin gömüldüğü belgeleri açabilir.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
