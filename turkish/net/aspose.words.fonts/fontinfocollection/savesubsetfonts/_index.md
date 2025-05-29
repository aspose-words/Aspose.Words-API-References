---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: .NET için Aspose.Words
description: FontInfoCollection SaveSubsetFonts özelliğini keşfedin, optimize edilmiş dosya boyutu ve performans için belgelerinizdeki gömülü TrueType yazı tipi alt kümelerini kontrol edin.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Gömülü TrueType yazı tiplerinin bir alt kümesinin belgeyle birlikte kaydedilip kaydedilmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`.

Bu seçenek yalnızca şu durumlarda çalışır:[`EmbedTrueTypeFonts`](../embedtruetypefonts/) mülk ayarlandı`doğru`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Notlar

Bu seçenek yalnızca DOC, DOCX ve RTF biçimleri için çalışır.

## Örnekler

TrueType yazı tiplerinin gömülü olduğu bir belgenin nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Ayrıca bakınız

* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
