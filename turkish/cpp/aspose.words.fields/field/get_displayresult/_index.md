---
title: "Aspose::Words::Fields::Field::get_DisplayResult metodu"
linktitle: "get_DisplayResult"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_DisplayResult metodu. C++'ta görüntülenen alan sonucunu temsil eden metni alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Görüntülenen alan sonucunu temsil eden metni alır.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Örnekler



Bir alanın belgede gösterdiği gerçek metni nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// DisplayResult özelliğini, tam olarak hangi metnin olduğunu doğrulamak için kullanabiliriz
// bir alanın belgede kendi yerinde göstereceği metni.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Alanlar gerçek zamanlı olarak doğru sonuç değerlerini tutmaz.
// Alanlarımızın her zaman doğru sonuçları göstermesini sağlamak için,
// örneğin bir kaydetme işleminden hemen önce, onları manuel olarak güncellememiz gerekir.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
