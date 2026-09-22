---
title: "Aspose::Words::Properties::DocumentPropertyCollection sınıfı"
linktitle: "DocumentPropertyCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentPropertyCollection sınıfı. BuiltInDocumentProperties ve CustomDocumentProperties koleksiyonları için temel sınıf. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


BuiltInDocumentProperties ve CustomDocumentProperties koleksiyonları için temel sınıf. Daha fazla bilgi edinmek için [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) belge makalesini ziyaret edin.

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Koleksiyondaki tüm özellikleri kaldırır. |
| [Contains](./contains/)(const System::String\&) | Koleksiyonda belirtilen ada sahip bir özellik varsa **true** döndürür. |
| [get_Count](./get_count/)() | Koleksiyondaki öğe sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Özelliğin adıyla bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [idx_get](./idx_get/)(int32_t) | İndeksle bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [IndexOf](./indexof/)(const System::String\&) | Bir özelliğin adını kullanarak indeksini alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Koleksiyondan belirtilen ada sahip bir özelliği kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir özelliği kaldırır. |
| static [Type](./type/)() |  |
## Açıklamalar


Özellik adları büyük/küçük harfe duyarsızdır.

Koleksiyondaki özellikler ada göre alfabetik olarak sıralanır.

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
