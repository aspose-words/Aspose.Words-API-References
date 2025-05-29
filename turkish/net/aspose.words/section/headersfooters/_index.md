---
title: Section.HeadersFooters
linktitle: HeadersFooters
articleTitle: HeadersFooters
second_title: .NET için Aspose.Words
description: Sezgisel özellik özelliğimizle bölüm başlıklarına ve altbilgilerine zahmetsizce erişin ve yönetin. Belge organizasyonunu ve sunumunu bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

Bölümün başlık ve altbilgi düğümlerine erişim sağlar.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

## Örnekler

Bir belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Bir belgeden tüm altbilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü inceleyin ve her türlü altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    // Üç çeşit altbilgi ve üstbilgi türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Çift" üstbilgisi/altbilgisi.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Ayrıca bakınız

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
