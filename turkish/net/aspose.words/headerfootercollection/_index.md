---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: .NET için Aspose.Words
description: Section HeaderFooter düğümlerine kolay, yazılı erişim için Aspose.Words.HeaderFooterCollection'ı keşfedin, belge yönetimini kolaylaştırın ve iş akışınızı geliştirin.
type: docs
weight: 3540
url: /tr/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Yazılı erişim sağlar[`HeaderFooter`](../headerfooter/) bir düğümün[`Section`](../section/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Üstbilgiler ve Altbilgilerle Çalışma](https://docs.aspose.com/words/net/working-with-headers-and-footers/) belgeleme makalesi.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Birini alır[`HeaderFooter`](../headerfooter/) verilen indekste. (3 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgilere ve altbilgilere bağlar veya bağlantısını kaldırır. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Belirtilen üstbilgi veya altbilgiyi önceki bölümdeki karşılık gelen üstbilgi veya altbilgiye bağlar veya bağlantısını kaldırır. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Tümünü kopyalar`ÜstbilgiAltbilgi` koleksiyondan yeni bir diziye`ÜstbilgiAltbilgi` s. (2 methods) |

## Notlar

En fazla bir tane olabilir[`HeaderFooter`](../headerfooter/)

her birinin[`HeaderFooterType`](../headerfootertype/) x000d_ başına[`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) nesneler koleksiyonda herhangi bir sırada bulunabilir.

## Örnekler

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

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. Bu paragraftaki metin
// bu bölümün her sayfasının en üstünde, ana gövde metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. Bu paragraftaki metin
// Bu bölümün her sayfasının en altında, ana gövde metninin altında görünecektir.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Ayrıca bakınız

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
