---
title: "Aspose::Words::Fields::FieldIndex::get_UseYomi metodu"
linktitle: "get_UseYomi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_UseYomi metodu. C++'de dizin girişleri için yomi metninin kullanılmasını etkinleştirip etkinleştirmeyeceğini alır veya ayarlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.fields/fieldindex/get_useyomi/
---
## FieldIndex::get_UseYomi method


Dizin girişleri için yomi metninin kullanımını etkinleştirip etkinleştirilmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_UseYomi()
```


## Örnekler



INDEX alanı girişlerini fonetik olarak nasıl sıralayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// INDEX tablosu, girişlerini otomatik olarak Text özelliklerinin değerlerine göre alfabetik sırayla sıralar.
// INDEX tablosunu, girişleri Hiragana kullanarak fonetik olarak sıralayacak şekilde ayarlayın.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// 4 XE alanı ekleyin; bu alanlar INDEX alanının içindekiler tablosunda giriş olarak görünecektir.
// "Text" özelliği, telaffuzu belirsiz olabilecek bir kelimenin Kanji yazımını içerebilir,
// öte yandan, kelimenin "Yomi" versiyonu, Hiragana kullanarak tam olarak nasıl telaffuz edildiğini gösterir.
// INDEX alanımızı Yomi kullanacak şekilde ayarlarsak, bu girişleri sıralayacaktır
// Yomi özelliklerinin değeriyle, Text değerleri yerine.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
