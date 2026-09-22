---
title: "Aspose::Words::Properties::CustomDocumentProperties class"
linktitle: "CustomDocumentProperties"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::CustomDocumentProperties class. Özel belge özelliklerinin bir koleksiyonudur. Daha fazla bilgi için C++'deki belge makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Özel belge özelliklerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Yeni bir özel belge özelliği, [String](../propertytype/) veri tipinde oluşturur. |
| [Add](./add/)(const System::String\&, int32_t) | Yeni bir özel belge özelliği, [Number](../propertytype/) veri tipinde oluşturur. |
| [Add](./add/)(const System::String\&, System::DateTime) | Yeni bir özel belge özelliği, [DateTime](../propertytype/) veri tipinde oluşturur. |
| [Add](./add/)(const System::String\&, bool) | Yeni bir özel belge özelliği, [Boolean](../propertytype/) veri tipinde oluşturur. |
| [Add](./add/)(const System::String\&, double) | Yeni bir özel belge özelliği, [Double](../propertytype/) veri tipinde oluşturur. |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | İçeriğe bağlı yeni bir özel belge özelliği oluşturur. |
| [Clear](../documentpropertycollection/clear/)() | Koleksiyondaki tüm özellikleri kaldırır. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Koleksiyonda belirtilen ada sahip bir özellik varsa **true** döndürür. |
| [get_Count](../documentpropertycollection/get_count/)() | Koleksiyondaki öğe sayısını alır. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Özelliğin adıyla bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | İndeksle bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Bir özelliğin adını kullanarak indeksini alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Koleksiyondan belirtilen ada sahip bir özelliği kaldırır. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Belirtilen indeksteki bir özelliği kaldırır. |
| static [Type](./type/)() |  |
## Açıklamalar


Her bir [DocumentProperty](../documentproperty/) nesnesi, bir kapsayıcı belgenin özel bir özelliğini temsil eder.

Özellik adları büyük/küçük harfe duyarsızdır.

Koleksiyondaki özellikler ada göre alfabetik olarak sıralanır.

## Örnekler



Özel belge özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Her belge, yerleşik özellikler gibi anahtar‑değer çiftleri olan bir özel özellik koleksiyonu içerir.
// Belgenin sabit bir yerleşik özellik listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
