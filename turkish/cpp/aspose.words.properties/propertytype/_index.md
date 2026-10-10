---
title: "Aspose::Words::Properties::PropertyType enum"
linktitle: "PropertyType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::PropertyType enum. C++'da bir belge özelliğinin veri tipini belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.properties/propertytype/
---
## PropertyType enum


Bir belge özelliğinin veri tipini belirtir.

```cpp
enum class PropertyType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Boolean | 0 | Özellik bir boolean değeridir. |
| DateTime | 1 | Özellik bir tarih saat değeridir. |
| Çift | 2 | Özellik bir kayan nokta sayıdır. |
| Number | 3 | Özellik bir tam sayı değeridir. |
| String | 4 | Özellik bir dize değeridir. |
| StringArray | 5 | Özellik bir dize dizisidir. |
| ObjectArray | 6 | Özellik bir nesne dizisidir. |
| ByteArray | 7 | Özellik bir bayt dizisidir. |
| Diğer | 8 | Özellik başka bir türdür. |


## Örnekler



Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Belgedeki tüm özel özellikleri yazdır.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// DOCPROPERTY alanı kullanarak bir özel özelliğin değerini göster.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Bu özel özellikleri Microsoft Word'de \"File\" -> \"Properties\" > \"Advanced Properties\" > \"Custom\" yoluyla bulabiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu verilmiştir.
// 1 -  İndekse göre kaldır:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  İsme göre kaldır:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Tüm koleksiyonu bir kerede boşalt:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
