---
title: "Aspose::Words::Fields::FieldAuthor::get_AuthorName yöntemi"
linktitle: "get_AuthorName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAuthor::get_AuthorName metodu. Belgenin yazarının adını alır veya ayarlar C++'ta."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldauthor/get_authorname/
---
## FieldAuthor::get_AuthorName method


Belgenin yazar adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldAuthor::get_AuthorName()
```


## Örnekler



Bir AUTHOR alanını kullanarak belge oluşturucusunun adını nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTHOR alanları sonuçlarını "Author" adlı yerleşik belge özelliğinden alır.
// Microsoft Word'de bir belge oluşturup kaydedersek,
// bu özellikte kullanıcı adımız olacaktır.
// Ancak, Aspose.Words kullanarak programlı bir şekilde belge oluşturursak,
// "Author" özelliği, varsayılan olarak, boş bir dize olacaktır.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// AUTHOR alanlarının kullanması için bir yedek yazar adı ayarlayın
// eğer "Author" özelliği boş bir dize içeriyorsa.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Bir değere sahip AUTHOR alanını güncellemek
// bu değeri "Author" yerleşik özelliğine uygular.
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Bu özelliği değiştirip ardından AUTHOR alanını güncellediğinizde, bu değer alanına uygulanır.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// "Name" özelliğini değiştirdikten sonra bir AUTHOR alanını güncellerseniz,
// sonra alan yeni adı görüntüleyecek ve yeni adı yerleşik özelliğe uygulayacak.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// AUTHOR alanları DefaultDocumentAuthor özelliğini etkilemez.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Ayrıca Bakınız

* Class [FieldAuthor](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
