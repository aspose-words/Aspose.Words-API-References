---
title: FontInfoCollection.EmbedTrueTypeFonts
second_title: Aspose.Words for .NET API Referansı
description: FontInfoCollection mülk. Belge kaydedildiğinde TrueType yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeriYANLIŞ .
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Belge kaydedildiğinde TrueType yazı tiplerinin belgeye gömülüp gömülmeyeceğini belirtir. Bu özelliğin varsayılan değeri:`YANLIŞ` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

### Notlar

TrueType yazı tiplerini gömmek, başkalarının belgeyi oluşturmak için kullanılan yazı tipleriyle aynı ile görüntülemesine olanak tanır, ancak belge boyutunu önemli ölçüde artırabilir.

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


