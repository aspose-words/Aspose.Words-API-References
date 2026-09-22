---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber method"
linktitle: "get_RevisionNumber"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber yöntemi. C++'ta belge revizyon numarasını alır veya ayarlar."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


Belge revizyon numarasını alır veya ayarlar.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## Açıklamalar


Aspose.Words bu özelliği güncellemez.

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


REVNUM alanlarıyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// Belgenin mevcut revizyon numarası özelliğini gösteren bir REVNUM alanı ekleyin.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// Bu özellik, bir belgenin Microsoft Word'de kaç kez kaydedildiğini sayar,
// ve izlenen revizyonlarla ilgili değildir. Windows Gezgini'nde belgeye sağ tıklayarak bulabiliriz
// Özellikler -> Ayrıntılar üzerinden. Bu özelliği manuel olarak güncelleyebiliriz.
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
