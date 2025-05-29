---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: .NET için Aspose.Words
description: Güçlü özellikler ve esneklikle belge bölümlerini etkili bir şekilde yönetmek için başvuracağınız çözüm olan Aspose.Words.SectionCollection sınıfını keşfedin.
type: docs
weight: 6570
url: /tr/net/aspose.words/sectioncollection/
---
## SectionCollection class

Bir koleksiyon[`Section`](../section/) belgedeki nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bölümlerle Çalışma](https://docs.aspose.com/words/net/working-with-sections/) belgeleme makalesi.

```csharp
public class SectionCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Belirtilen dizindeki bir bölümü alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Koleksiyondaki tüm bölümleri yeni bir bölüm dizisine kopyalar. (2 methods) |

## Notlar

Bir Microsoft Word belgesi birden fazla bölüm içerebilir. Microsoft Word'de bir bölüm oluşturmak için, Ekle/Break komutunu seçin ve bir kesme türü seçin. Kesme, bölümün yeni bir sayfada mı yoksa aynı sayfada mı başlayacağını belirtir.

Bölümleri programlı olarak eklemek ve kaldırmak, posta birleştirme sırasında üretilen belgeleri özelleştirmek için kullanılabilir. Bir belgenin bazı ölçütlere bağlı olarak farklı içeriğe veya içeriğinin parçalarına sahip olması gerekiyorsa, birden fazla bölüm içeren bir "ana" belge oluşturabilir ve posta birleştirmeden önce veya sonra bölümlerden bazılarını silebilirsiniz.

## Örnekler

Bir belgeye bölümlerin nasıl ekleneceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Belgeden ilk bölümü sil.
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
