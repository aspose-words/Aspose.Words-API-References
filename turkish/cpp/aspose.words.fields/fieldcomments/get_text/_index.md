---
title: "Aspose::Words::Fields::FieldComments::get_Text yöntemi"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldComments::get_Text yöntemi. Yorumların metnini C++'ta alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Yorumların metnini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Örnekler



COMMENTS alanını nasıl kullanacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin "Comments" yerleşik özelliği için bir değer ayarlayın.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Bu yerleşik özelliğin değerini göstermek için bir COMMENTS alanı oluşturun.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// COMMENTS alanının Text özelliği değerini verip güncellerseniz, alan şunu yapacaktır
// "Comments" yerleşik özelliğinin mevcut değerini, Text özelliğinin değeriyle üzerine yazar,
// ve ardından yeni değeri gösterir.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Ayrıca Bakınız

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
