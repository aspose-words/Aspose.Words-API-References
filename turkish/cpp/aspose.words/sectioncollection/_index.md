---
title: "Aspose::Words::SectionCollection sınıfı"
linktitle: "SectionCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SectionCollection sınıfı. Belgedeki Section nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 59000
url: /tr/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Belgedeki [Section](../section/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) dokümantasyon makalesini ziyaret edin.

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümü koleksiyonun sonuna ekler. |
| [Clear](../nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get_Count](../nodecollection/get_count/)() | Koleksiyondaki düğüm sayısını alır. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen indeksdeki bölümü getirir. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen indeksde bir düğümü koleksiyona ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](./toarray/)() | Koleksiyondaki tüm bölümleri yeni bir bölüm dizisine kopyalar. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir Microsoft Word belgesi birden fazla bölüm içerebilir. Microsoft Word'de bir bölüm oluşturmak için Ekle/Kesme komutunu seçin ve bir kesme türü belirleyin. Kesme, bölümün yeni bir sayfada mı yoksa aynı sayfada mı başlayacağını belirtir.

Programlı olarak bölümleri eklemek ve kaldırmak, posta birleştirme sırasında oluşturulan belgeleri özelleştirmek için kullanılabilir. Bir belgenin bazı kriterlere bağlı olarak farklı içeriklere veya içerik parçalarına sahip olması gerekiyorsa, birden fazla bölüm içeren bir "ana" belge oluşturabilir ve posta birleştirmeden önce veya sonra bazı bölümleri silebilirsiniz.

## Örnekler



Bir belgede bölümleri ekleme ve kaldırma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Belgedeki ilk bölümü sil.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Şu anda ilk bölüm olanın bir kopyasını belgenin sonuna ekle.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
