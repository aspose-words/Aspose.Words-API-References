---
title: "Aspose::Words::Fields::FieldIndex sınıfı"
linktitle: "FieldIndex"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex sınıfı. INDEX alanını uygular. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 59000
url: /tr/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


INDEX alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır veya ayarlar. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Çapraz referansları ve diğer girişleri ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_EntryType](./get_entrytype/)() | Dizini oluşturmak için kullanılan bir indeks girişi tipini alır veya ayarlar. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Alan kodu aracılığıyla bir sayfa numarası ayırıcısının geçersiz kılınıp kılınmadığını gösteren bir değeri alır. |
| [get_HasSequenceName](./get_hassequencename/)() | Alan sonucunun oluşturulması sırasında bir dizinin kullanılıp kullanılmayacağını gösteren bir değeri alır. |
| [get_Heading](./get_heading/)() | Belirli bir harf için giriş setlerinin başında görünen bir başlığı alır veya ayarlar. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LanguageId](./get_languageid/)() | Dizini oluşturmak için kullanılan dil kimliğini alır veya ayarlar. |
| [get_LetterRange](./get_letterrange/)() | Dizini sınırlayan bir harf aralığını alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Dizini oluştururken sayfa başına kullanılan sütun sayısını alır veya ayarlar. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Sayfa numarası listesinde iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Dizin girişini ve sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Sayfa aralığının başlangıç ve sonunu ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Alt girişlerin ana girişle aynı satıra yerleştirilip yerleştirilmeyeceğini alır veya ayarlar. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_SequenceName](./get_sequencename/)() | Sayfa numarasıyla birlikte numarası eklenen bir dizinin adını alır veya ayarlar. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [get_UseYomi](./get_useyomi/)() | Dizin girişleri için yomi metninin kullanımını etkinleştirip etkinleştirilmeyeceğini alır veya ayarlar. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/). |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/). |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/). |
| [set_Heading](./set_heading/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/). |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseYomi](./set_useyomi/)(bool) | Ayarlayıcı for [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
