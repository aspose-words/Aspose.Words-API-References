---
title: "Aspose::Words::Fields::FieldKeywords::get_Text yöntemi"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldKeywords::get_Text yöntemi. C++'ta anahtar kelimelerin metnini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Anahtar kelimelerin metnini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Örnekler



Bir KEYWORDS alanı eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dosya Gezgini'nde "etiketler" olarak da adlandırılan bazı anahtar kelimeler ekleyin.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// KEYWORDS alanı bu özelliğin değerini gösterir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Alanının Text özelliği için bir değer ayarlamak,
// ve ardından alanı güncellemek, ilgili yerleşik özelliği yeni değerle de üzerine yazar.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Ayrıca Bakınız

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
