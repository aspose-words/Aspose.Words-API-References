---
title: "Aspose::Words::Markup::CustomPartCollection class"
linktitle: "CustomPartCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomPartCollection class. CustomPart nesnelerinden oluşan bir koleksiyon temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class


[CustomPart](../custompart/) nesnelerinden oluşan bir koleksiyon temsil eder. Daha fazla bilgi edinmek için [Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomPart>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Koleksiyona bir öğe ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](./clone/)() | Bu koleksiyonun ve öğelerinin derin bir kopyasını oluşturur. |
| [CustomPartCollection](./custompartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\&) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir öğeyi kaldırır. |
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


Normalde bu sınıfın örneklerini oluşturmanız gerekmez. OOXML paketine ilişkin özel bölümlere [PackageCustomParts](../../aspose.words/document/get_packagecustomparts/) özelliği aracılığıyla erişirsiniz.

## Örnekler



Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// İkinci bölümü kopyalayın, ardından kopyayı koleksiyona ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Koleksiyonu döngüyle gezerek her bölümü yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Bu koleksiyondan öğeleri tek tek ya da toplu olarak kaldırabiliriz.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
