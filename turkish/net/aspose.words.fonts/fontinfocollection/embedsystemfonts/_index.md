---
title: FontInfoCollection.EmbedSystemFonts
second_title: Aspose.Words for .NET API Referansı
description: FontInfoCollection mülk. Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeriYANLIŞ.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Sistem yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ`.

Bu seçenek yalnızca şu durumlarda çalışır:[`EmbedTrueTypeFonts`](../embedtruetypefonts/) seçenek şu şekilde ayarlandı:`doğru`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

### Notlar

Bu özelliği şuna ayarlıyoruz:`doğru`Kullanıcı bir Doğu Asya system kullanıyorsa ve sistemlerinde that dili için yazı tipleri bulunmayan diğer kişiler tarafından okunabilen bir belge oluşturmak istiyorsa kullanışlıdır. Örneğin, Japonca bir sistemdeki bir kullanıcı, Japonca belgenin tüm sistemlerde okunabilmesi için the yazı tiplerini bir belgeye yerleştirmeyi seçebilir.

Bu seçenek yalnızca DOC, DOCX ve RTF formatlarında çalışır.

### Örnekler

Gömülü TrueType yazı tiplerine sahip bir belgenin nasıl kaydedileceğini gösterir.

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


