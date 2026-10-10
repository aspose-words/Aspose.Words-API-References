---
title: "Aspose::Words::Fields::FieldSubject::get_Text yöntemi"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSubject::get_Text yöntemi. C++'ta konunun metnini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Subject'in metnini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Örnekler



SUBJECT alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Belgenin "Subject" yerleşik özelliği için bir değer ayarlayın.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Bu yerleşik özelliğin değerini göstermek için bir SUBJECT alanı oluşturun.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Eğer SUBJECT alanının Text özelliği değerini verir ve güncellerseniz, alan
// "Subject" yerleşik özelliğinin mevcut değerini, Text özelliğinin değeriyle üzerine yazar,
// ve ardından yeni değeri gösterir.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Ayrıca Bakınız

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
