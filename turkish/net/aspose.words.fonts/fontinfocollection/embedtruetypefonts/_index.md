---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: .NET için Aspose.Words
description: FontInfoCollection'daki EmbedTrueTypeFonts özelliğinin TrueType font gömülmesine izin vererek belge kalitesini nasıl artırdığını öğrenin. Varsayılan değer false'tur.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Bir belge kaydedildiğinde TrueType yazı tiplerinin gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri`YANLIŞ` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Notlar

TrueType yazı tiplerini yerleştirmek, başkalarının belgeyi oluşturmak için kullanılan yazı tipleriyle görüntülemesine olanak tanır, ancak belge boyutunu önemli ölçüde artırabilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatları için çalışır.

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
