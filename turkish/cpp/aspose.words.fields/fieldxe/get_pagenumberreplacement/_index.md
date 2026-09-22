---
title: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement metodu"
linktitle: "get_PageNumberReplacement"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement metodu. C++'da bir sayfa numarası yerine kullanılan metni alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fieldxe/get_pagenumberreplacement/
---
## FieldXE::get_PageNumberReplacement method


Sayfa numarası yerine kullanılan metni alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageNumberReplacement()
```


## Örnekler



Bir INDEX alanında çapraz referansların nasıl tanımlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgedeki her XE alanı için bir giriş gösteren bir INDEX alanı oluşturun.
// Her giriş, XE alanının Text özelliği değerini sol tarafta gösterir,
// ve XE alanını içeren sayfanın numarasını sağ tarafta.
// INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacaktır
// her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişte birleştirir.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Bir XE alanını, INDEX girişinin bir sayfa numarası yerine bir dize göstermesi için yapılandırabiliriz.
// İlk olarak, bir sayfa numarasını bir dizeyle değiştiren girişler için,
// XE alanının Text özelliği değeri ile dize arasında özel bir ayırıcı belirtin.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Bu alanın sayfa numarasını gösteren normal bir INDEX girişi oluşturan bir XE alanı ekleyin,
// ve CrossReferenceSeparator değerini çağırmaz.
// Bu XE alanı için giriş "Apple, 2" olarak gösterilecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Sayfa 3'te başka bir XE alanı ekleyin ve PageNumberReplacement özelliği için bir değer ayarlayın.
// Bu değer, bu alanın bulunduğu sayfanın numarası yerine görünecektir,
// ve INDEX alanının CrossReferenceSeparator değeri onun önünde görünecektir.
// Bu XE alanı için giriş "Muz, bkz: Tropikal meyve" olarak gösterilecektir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Ayrıca Bakınız

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
