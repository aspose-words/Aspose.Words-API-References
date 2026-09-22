---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime method"
linktitle: "get_LastSavedTime"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime yöntemi. C++'ta son kaydetme zamanını UTC olarak alır veya ayarlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Son kaydetme zamanını UTC olarak alır veya ayarlar.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Açıklamalar


RTF formatından gelen belgeler için bu özellik, son kaydetme işleminin yerel zamanını döndürür.

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


Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Belgedeki son kaydetme işleminin tarih ve saatini göstermek için SAVEDATE alanını kullanabiliriz.
// Bu alanların referans aldığı kaydetme işlemi, Microsoft Word gibi bir uygulamadaki manuel kaydetmedir,
// belgenin Save metodundan değildir.
// Aşağıda, SAVEDATE alanının tarih/saat görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 -  İslami Ay Takvimi:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura takvimi:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - Hint Ulusal takvimi:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// SAVEDATE alanları tarih/saat değerlerini LastSavedTime yerleşik özelliğinden alır.
// Belgenin Save metodu bu değeri güncellemez, ancak yine de manuel olarak güncelleyebiliriz.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
