---
title: "Aspose::Words::Fields::FieldTitle::get_Text metodu"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldTitle::get_Text yöntemi. C++'ta başlığın metnini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Başlığın metnini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Örnekler



TITLE alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yerleşik "Title" belge özelliği için bir değer ayarlayın.
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Bu özelliğin değerini belgede göstermek için TITLE alanını kullanabiliriz.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Alanının Text özelliği için bir değer ayarlamak,
// ve ardından alanı güncellemek, ilgili yerleşik özelliği yeni değerle de üzerine yazar.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## Ayrıca Bakınız

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
