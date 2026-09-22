---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove metodu"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove metodu. C++'ta koleksiyondan belirtilen adla bir yer imini kaldırır."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/remove/
---
## BookmarksOutlineLevelCollection::Remove method


Koleksiyondan belirtilen ada sahip bir yer imini kaldırır.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Yer iminin büyük/küçük harfe duyarsız adı. |

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

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
