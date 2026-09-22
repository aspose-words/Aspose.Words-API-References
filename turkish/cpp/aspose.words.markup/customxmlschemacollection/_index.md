---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection sınıfı"
linktitle: "CustomXmlSchemaCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection sınıfı. Özel bir XML bölümüne bağlı XML şemalarını temsil eden dizelerin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Özel bir XML bölümüyle ilişkili XML şemalarını temsil eden dize koleksiyonudur. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::String\&) | Koleksiyona bir öğe ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](./clone/)() | Bu nesnenin derin bir klonunu oluşturur. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [IndexOf](./indexof/)(const System::String\&) | Koleksiyondaki belirtilen değerin sıfır tabanlı indeksini döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir değeri kaldırır. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Bu sınıfın örneklerini oluşturmazsınız. Özel bir XML bölümünün XML şemaları koleksiyonuna [Schemas](../customxmlpart/get_schemas/) özelliği aracılığıyla erişirsiniz.

## Örnekler



Bir XML şema koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Bir XML şema ilişkilendirmesi ekleyin.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Özel XML bölümünün XML şema ilişkilendirme koleksiyonunu klonlayın,
// ve ardından klona birkaç yeni şema ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları sıralayın ve her öğeyi yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Aşağıda koleksiyondan şema kaldırmanın üç yolu verilmiştir.
// 1 -  Şemayı indeksine göre kaldır:
schemas->RemoveAt(2);

// 2 -  Şemayı değerine göre kaldır:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  \"Clear\" yöntemini kullanarak koleksiyonu bir kerede boşaltın.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
