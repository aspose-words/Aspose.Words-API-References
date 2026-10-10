---
title: "Aspose::Words::Fields::FieldIndex::get_BookmarkName metodu"
linktitle: "get_BookmarkName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_BookmarkName metodu. C++'ta dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işareti adını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldindex/get_bookmarkname/
---
## FieldIndex::get_BookmarkName method


Dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_BookmarkName()
```


## Örnekler



INDEX alanı nasıl oluşturulacağını ve ardından XE alanlarını kullanarak girişlerle doldurulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek
// ve XE alanını içeren sayfayı sağ tarafta.
// Eğer XE alanlarının "Text" özelliğindeki değer aynı ise,
// INDEX alanı onları tek bir girişte gruplayacak.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// INDEX alanını yalnızca sınırlar içinde olan XE alanlarını gösterecek şekilde yapılandırın
// "MainBookmark" adlı bir yer işareti içinde ve "EntryType" özelliklerinin "A" değerine sahip olan.
// Hem INDEX hem de XE alanları için, "EntryType" özelliği yalnızca dize değerinin ilk karakterini kullanır.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// Yeni bir sayfada, yer işaretini değere eşleşen bir adla başlatın
// INDEX alanının "BookmarkName" özelliğinin değerine.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// INDEX alanı bu girişi, yer işareti içinde olduğu için alacaktır,
// ve giriş tipi de INDEX alanının giriş tipiyle eşleşir.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Giriş tipleri eşleşmediği için INDEX'te görünmeyecek bir XE alanı ekleyin.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Yer işaretini sonlandırın ve ardından bir XE alanı ekleyin.
// INDEX alanı ile aynı tipe sahiptir, ancak görünmeyecek
// çünkü yer işareti sınırlarının dışındadır.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
