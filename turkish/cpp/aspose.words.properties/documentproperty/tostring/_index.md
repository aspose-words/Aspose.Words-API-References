---
title: "Aspose::Words::Properties::DocumentProperty::ToString metodu"
linktitle: "ToString"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentProperty::ToString metodu. C++'ta geçerli yerel ayara göre biçimlendirilmiş bir dize olarak özellik değerini döndürür."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Özellik değerini geçerli yerel ayara göre biçimlendirilmiş bir dize olarak döndürür.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Açıklamalar


Bir boolean özelliği "Y" veya "N" değerine dönüştürür. Bir tarih özelliğini kısa tarih dizesine dönüştürür. Diğer tüm tipler için özelliği Object.ToString() kullanarak dönüştürür.

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


Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## Ayrıca Bakınız

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
