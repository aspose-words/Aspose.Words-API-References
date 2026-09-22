---
title: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator metodu"
linktitle: "get_HasPageNumberSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator metodu. C++'da alan kodu aracılığıyla bir sayfa numarası ayırıcıyı geçersiz kılıp kılmadığını gösteren bir değer alır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fieldindex/get_haspagenumberseparator/
---
## FieldIndex::get_HasPageNumberSeparator method


Alan kodu aracılığıyla bir sayfa numarası ayırıcısının geçersiz kılınıp kılınmadığını gösteren bir değeri alır.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasPageNumberSeparator()
```


## Örnekler



Bir INDEX alanında sayfa numarası ayırıcıyı nasıl düzenleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip XE alanlarını gruplayacak
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Eğer INDEX alanımız bir grup XE alanı için bir giriş içeriyorsa,
// Bu giriş, bu gruba ait bir XE alanı içeren her sayfanın numarasını gösterecektir.
// Bu sayfa numaralarının görünümünü özelleştirmek için özel ayırıcılar ayarlayabiliriz.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// Bu XE alanlarını ekledikten sonra, INDEX alanı "First entry, on page(s) 2 & 3 & 4" ifadesini gösterecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## Ayrıca Bakınız

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
