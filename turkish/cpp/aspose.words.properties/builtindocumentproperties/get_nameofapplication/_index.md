---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication yöntemi"
linktitle: "get_NameOfApplication"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication yöntemi. C++'ta uygulamanın adını alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_nameofapplication/
---
## BuiltInDocumentProperties::get_NameOfApplication method


Uygulamanın adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication()
```


## Örnekler



"Origin" kategorisindeki belge özellikleriyle nasıl çalışılacağını gösterir.
```cpp
// Microsoft Word kullanarak oluşturduğumuz ve düzenlediğimiz bir belgeyi açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Aşağıdaki yerleşik özellikler, bu belgenin oluşturulması ve düzenlenmesiyle ilgili bilgileri içerir.
// Bu belgeyi Windows Gezgini'nde sağ tıklayıp bulabiliriz
// bu özellikleri "Properties" -> "Details" -> "Origin" kategorisi üzerinden bulabilirsiniz.
// PRINTDATE ve EDITTIME gibi alanlar, bu değerleri belge gövdesinde görüntüleyebilir.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Yerleşik özelliklerin değerlerini de değiştirebiliriz.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word, belgeyi kaydettiğimizde aşağıdaki özellikleri otomatik olarak günceller.
// Bu özellikleri Aspose.Words ile kullanmak için, değerlerini manuel olarak ayarlamamız gerekir.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Bu belgeyi Windows Gezgini'nde sağ tıklayıp bu özellikleri "Properties" -> "Details" -> "Origin" içinde bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
