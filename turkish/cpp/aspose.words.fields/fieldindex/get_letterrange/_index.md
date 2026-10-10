---
title: "Aspose::Words::Fields::FieldIndex::get_LetterRange metodu"
linktitle: "get_LetterRange"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_LetterRange metodu. C++'ta dizini sınırlayan harf aralığını alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fields/fieldindex/get_letterrange/
---
## FieldIndex::get_LetterRange method


Dizini sınırlayan bir harf aralığını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_LetterRange()
```


## Örnekler



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

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
