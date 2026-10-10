---
title: "Aspose::Words::Fields::FieldXE::get_Text metodu"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldXE::get_Text metodu. Girişin metnini alır veya ayarlar C++'ta."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fields/fieldxe/get_text/
---
## FieldXE::get_Text method


Girişin metnini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Text()
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


XE alanlarını kullanarak bir INDEX alanını girişlerle doldurmayı ve ayrıca görünümünü değiştirmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// Eğer XE alanlarının "Text" özelliğindeki değer aynı ise,
// INDEX alanı onları tek bir girişte gruplayacak.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Bu özelliğin değerini "A" olarak ayarlamak, tüm girişleri ilk harflerine göre gruplandırır,
// ve bu harfi her grubun üstünde büyük harfle yerleştirir.
index->set_Heading(u"A");

// INDEX alanı tarafından oluşturulan tabloyu 2 sütun boyunca genişletecek şekilde ayarlayın.
index->set_NumberOfColumns(u"2");

// "a-c" karakter aralığının dışındaki başlangıç harflerine sahip tüm girişleri atlanacak şekilde ayarlayın.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Bu iki sonraki XE alanı, "A" başlığı altında görünecek,
// ve ilgili metin stilleri sayfa numaralarına da uygulanacaktır.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// İki sonraki XE alanı, INDEX alanlarının içindekiler tablosunda "B" ve "C" başlıkları altında yer alacaktır.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// INDEX alanları tüm girişleri alfabetik olarak sıralar, bu yüzden bu giriş diğer ikisiyle birlikte "A" altında görünecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Bu giriş, "D" harfiyle başladığı için görünmeyecektir,
// bu, INDEX alanının LetterRange özelliğinin tanımladığı "a-c" karakter aralığının dışındadır.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Ayrıca Bakınız

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
