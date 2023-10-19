---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.SectionCollection sınıf. Bir koleksiyonSection belgedeki nesneler C#'da.
type: docs
weight: 5740
url: /tr/net/aspose.words/sectioncollection/
---
## SectionCollection class

Bir koleksiyon[`Section`](../section/) belgedeki nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bölümlerle Çalışmak](https://docs.aspose.com/words/net/working-with-sections/) dokümantasyon makalesi.

```csharp
public class SectionCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Verilen dizindeki bir bölümü alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tüm düğümleri bu koleksiyondan ve belgeden kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Koleksiyondaki tüm bölümleri yeni bir bölüm dizisine kopyalar. (2 methods) |

## Notlar

Bir Microsoft Word belgesi birden fazla bölüm içerebilir. Microsoft Word'de bir bölüm oluşturmak için Ekle/Bırak komutunu seçin ve bir kesme türü seçin. Ara, bölümün ile yeni bir sayfada mı yoksa aynı sayfada mı başlayacağını belirtir.

Adres-mektup birleştirme sırasında üretilen belgelerini özelleştirmek için programlı olarak bölüm ekleme ve kaldırma kullanılabilir. Bir belgenin bazı kriterlere bağlı olarak farklı içeriğe veya the içeriğinin bölümlerine sahip olması gerekiyorsa, o zaman birden fazla bölüm içeren bir "ana" belge oluşturabilir ve adres-mektup birleştirmeden önce veya sonra bazı bölümleri silebilirsiniz.

## Örnekler

Bir belgede bölümlerin nasıl eklenip kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Dokümanın ilk bölümünü silin.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Şimdi ilk bölümün bir kopyasını belgenin sonuna ekleyin.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
