---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection sınıfı"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection sınıfı. Bireysel yer imleri ana hat seviyesi koleksiyonu. Daha fazla bilgi edinmek için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


Bireysel yer imlerinin anahat düzeyinin bir koleksiyonu. Daha fazla bilgi için, [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) dokümantasyon makalesini ziyaret edin.

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Koleksiyona bir yer imi ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](./contains/)(const System::String\&) | Koleksiyonun verilen ada sahip bir yer imi içerip içermediğini belirler. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Yer imi adını kullanarak bir yer imi ana hat seviyesini alır veya ayarlar. |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir yer imi ana hat seviyesini alır veya ayarlar. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Yer imi adını kullanarak bir yer imi ana hat seviyesini alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Belirtilen indeksteki bir yer imi ana hat seviyesini alır veya ayarlar. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Koleksiyondaki belirtilen yer iminin sıfır tabanlı indeksini döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Koleksiyondan belirtilen ada sahip bir yer imini kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir yer imini kaldırır. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Anahtar, büyük/küçük harfe duyarsız bir dize yer imi adıdır. Değer, bir int yer imi ana hat seviyesidir.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

## Örnekler



Yer imleri için ana hat seviyelerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İçine başka bir yer imi gömülü bir yer imi ekle.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Başka bir yer imi ekle.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// PDF olarak kaydederken, yer imlerine açılır menü üzerinden erişilebilir ve çoğu okuyucu tarafından bağlantı olarak kullanılabilir.
// Yer imleri ayrıca anahat seviyeleri için sayısal değerlere sahip olabilir,
// okuyucuda daraltıldığında alt seviye anahat girişlerinin üst seviye alt girişleri gizlemesine olanak tanır.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Sadece "Bookmark 1" için anahat seviyesi atamasının kalması için iki öğeyi kaldırabiliriz.
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Dokuz anahat seviyesi vardır. Numaralandırmaları kaydetme işlemi sırasında optimize edilecektir.
// Bu durumda, "5" ve "9" seviyeleri "2" ve "3" olacaktır.
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Bu koleksiyonu boşaltmak yer imlerini koruyacak ve hepsini aynı anahat seviyesine yerleştirecektir.
outlineLevels->Clear();
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
