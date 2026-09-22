---
title: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine metodu"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine metodu. C++'ta alt girişlerin ana girişle aynı satıra konulup konulmayacağını alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Alt girişlerin ana girişle aynı satıra yerleştirilip yerleştirilmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Örnekler



Bir INDEX alanında alt girişlerle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// Değeri INDEX girişinin başlığı haline gelen bir Text özelliğine sahip XE alanları.
// Bu değer iki dize segmenti içeriyorsa ve iki nokta üst üste ile bölünmüşse (INDEX girişi :) ayırıcıyı kabul eder,
// ilk segment başlık, ikinci segment ise alt başlık olur.
// INDEX alanı önce girişleri alfabetik olarak gruplar, ardından aynı
// başlıklara sahip birden fazla XE alanı varsa, INDEX alanı bu başlıkların değerlerine göre daha da alt gruplara ayırır.
// Birden fazla alt grup katmanı olabilir, kaç kez
// XE alanlarının Text özellikleri bu şekilde bölündükçe.
// Varsayılan olarak, bir INDEX alanı giriş grubu bu grup içindeki her alt başlık için yeni bir satır oluşturur.
// Başlığı korumak için RunSubentriesOnSameLine bayrağını true olarak ayarlayabiliriz,
// ve grup içindeki tüm alt başlıkları aynı satırda tutar, bu da INDEX alanını daha kompakt hâle getirir.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// İki XE alanı ekleyin, her biri yeni bir sayfada ve aynı "Heading 1" başlığına sahip,
// bu başlığı INDEX alanı gruplamak için kullanacaktır.
// RunSubentriesOnSameLine false ise, INDEX tablosu üç satır oluşturur:
// "Heading 1" gruplama başlığı için bir satır ve her alt başlık için bir satır daha.
// RunSubentriesOnSameLine true ise, INDEX tablosu tek satırlık bir
// giriş oluşturur; bu giriş başlığı ve tüm alt başlıkları kapsar.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
