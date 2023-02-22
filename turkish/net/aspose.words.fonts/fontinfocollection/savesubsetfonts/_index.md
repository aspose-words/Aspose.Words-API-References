---
title: FontInfoCollection.SaveSubsetFonts
second_title: Aspose.Words for .NET API Referansı
description: FontInfoCollection mülk. Belge ile katıştırılmış TrueType yazı tiplerinin bir alt kümesinin kaydedilip kaydedilmeyeceğini belirtir. Bu özellik için varsayılan değer yanlış.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Belge ile katıştırılmış TrueType yazı tiplerinin bir alt kümesinin kaydedilip kaydedilmeyeceğini belirtir. Bu özellik için varsayılan değer **yanlış**.

Bu seçenek yalnızca şu durumlarda çalışır:[`EmbedTrueTypeFonts`](../embedtruetypefonts/) özellik olarak ayarlandı **doğru**.

```csharp
public bool SaveSubsetFonts { get; set; }
```

### Notlar

Bu seçenek yalnızca DOC, DOCX ve RTF biçimleri için çalışır.

### Örnekler

Bir belgenin gömülü TrueType yazı tipleriyle nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Ayrıca bakınız

* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../fontinfocollection/)
* toplantı [Aspose.Words](../../../)


