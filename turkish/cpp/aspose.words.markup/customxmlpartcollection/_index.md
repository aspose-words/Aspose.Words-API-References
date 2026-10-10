---
title: "Aspose::Words::Markup::CustomXmlPartCollection sınıfı"
linktitle: "CustomXmlPartCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlPartCollection sınıfı. Özel XML Bölümlerinin bir koleksiyonunu temsil eder. Öğeler CustomXmlPart nesneleridir. Daha fazla bilgi edinmek için C++'daki  dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class


Özel XML Bölümlerinin bir koleksiyonunu temsil eder. Öğeler [CustomXmlPart](../customxmlpart/) nesneleridir. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomXmlPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Koleksiyona bir öğe ekler. |
| [Add](./add/)(const System::String\&, const System::String\&) | Belirtilen XML ile yeni bir XML bölümü oluşturur ve koleksiyona ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Clone](./clone/)() | Bu koleksiyonun ve öğelerinin derin bir kopyasını oluşturur. |
| [CustomXmlPartCollection](./customxmlpartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetById](./getbyid/)(const System::String\&) | Bir tanımlayıcı ile özel bir XML bölümünü bulur ve döndürür. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
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


Genellikle bu sınıfın örneklerini oluşturmanız gerekmez. Bir belgede depolanan özel XML verilerine [CustomXmlParts](../../aspose.words/document/get_customxmlparts/) özelliği aracılığıyla erişebilirsiniz.

## Örnekler



Özel XML verileriyle yapılandırılmış belge etiketi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Veri içeren bir XML bölümü oluşturun ve belge koleksiyonuna ekleyin.
// Microsoft Word'de "Developer" sekmesini etkinleştirirsek,
// Bu koleksiyondan öğeleri "XML Mapping Pane" içinde, birkaç varsayılan öğe ile birlikte bulabiliriz.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Aşağıda XML bölümlerine başvurmanın iki yolu verilmiştir.
// 1 -  Özel XML bölüm koleksiyonunda bir indeksle:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  GUID ile:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Bir XML şema ilişkilendirmesi ekleyin.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Bir bölümü klonlayın ve ardından koleksiyona ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Koleksiyonu döngüyle gezerek her bölümün içeriğini yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Klonlanan bölümü indeksle kaldırmak için "RemoveAt" metodunu kullanın.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// XML bölüm koleksiyonunu klonlayın ve ardından tüm öğelerini bir anda kaldırmak için "Clear" metodunu kullanın.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Bölümümüzün içeriğini gösterecek bir yapılandırılmış belge etiketi oluşturun ve belge gövdesine ekleyin.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
