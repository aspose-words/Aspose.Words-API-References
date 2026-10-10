---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get yöntemi. C++'ta özelliğin adıyla bir DocumentProperty nesnesi döndürür."
type: docs
weight: 35000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Özelliğin adıyla bir [DocumentProperty](../../documentproperty/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | System::String | Alınacak özelliğin büyük/küçük harfe duyarsız adı. |
## Açıklamalar


[BuiltInDocumentProperties](../) tarafından sunulan tiplenmiş özelliklerin adlarıyla eşleşen dize adları.

Eğer belgede bulunmayan bir özelliği talep ederseniz, ancak özelliğin adı geçerli bir yerleşik ad olarak tanınıyorsa, yeni bir [DocumentProperty](../../documentproperty/) oluşturulur, koleksiyona eklenir ve döndürülür. Yeni oluşturulan özelliğe, yerleşik özelliğin türüne bağlı olarak (boş dize, sıfır, **false** veya DateTime.MinValue) varsayılan bir değer atanır.

Eğer belgede bulunmayan bir özelliği talep ederseniz ve ad bir yerleşik ad olarak tanınmazsa, **null** döndürülür.

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

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
