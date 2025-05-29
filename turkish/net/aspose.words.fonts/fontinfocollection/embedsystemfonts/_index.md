---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: .NET için Aspose.Words
description: FontInfoCollection EmbedSystemFonts özelliğinin sistem fontlarını gömerek belgelerinizi nasıl geliştirdiğini keşfedin. Varsayılan değerini ve avantajlarını öğrenin!
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`.

Bu seçenek yalnızca şu durumlarda çalışır:[`EmbedTrueTypeFonts`](../embedtruetypefonts/) seçenek ayarlandı`doğru`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Notlar

Bu özelliği şu şekilde ayarlamak:`doğru` kullanıcı Doğu Asya sistemindeyse ve sistemlerinde bu dil için yazı tipleri olmayan başkaları tarafından okunabilen bir belge oluşturmak istiyorsa yararlıdır. Örneğin, Japonca bir sistemdeki bir kullanıcı, Japonca belgenin tüm sistemlerde okunabilmesi için bir belgeye yazı tiplerini yerleştirmeyi seçebilir.

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
