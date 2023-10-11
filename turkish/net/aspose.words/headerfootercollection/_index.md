---
title: Class HeaderFooterCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.HeaderFooterCollection sınıf. Yazılı erişim sağlarHeaderFooter bir düğümSection .
type: docs
weight: 3110
url: /tr/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Yazılı erişim sağlar[`HeaderFooter`](../headerfooter/) bir düğüm[`Section`](../section/) .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Üstbilgiler ve Altbilgilerle Çalışmak](https://docs.aspose.com/words/net/working-with-headers-and-footers/) dokümantasyon makalesi.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Bir öğeyi alır[`HeaderFooter`](../headerfooter/) verilen dizinde. (3 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tüm düğümleri bu koleksiyondan ve belgeden kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(bool) | Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgilerine ve altbilgilerine bağlar veya bağlantısını kaldırır. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(HeaderFooterType, bool) | Belirtilen üstbilgiyi veya altbilgiyi önceki bölümdeki ilgili üstbilgiye veya altbilgiye bağlar veya bağlantısını kaldırır. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Tümünü kopyalar`BaşlıkAltbilgi` koleksiyondan yeni bir diziye`BaşlıkAltbilgi` s. (2 methods) |

### Notlar

En fazla bir tane olabilir[`HeaderFooter`](../headerfooter/)

her biri için[`HeaderFooterType`](../headerfootertype/) per [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) nesneler koleksiyonda herhangi bir sırada bulunabilir.

### Örnekler

Bir belgedeki tüm altbilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü yineleyin ve her türden altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    // Üç çeşit altbilgi ve başlık türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Çift" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının üst kısmında, ana metin metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının altında, ana gövde metninin altında görünecektir.
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


