---
title: "Aspose::Words::Properties::DocumentProperty sınıfı"
linktitle: "DocumentProperty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentProperty sınıfı. Özel veya yerleşik bir belge özelliğini temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Özel veya yerleşik bir belge özelliğini temsil eder. Daha fazla bilgi edinmek için [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) dokümantasyon makalesini ziyaret edin.

```cpp
class DocumentProperty : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Bu özelliğin içeriğe bağlı olup olmadığını gösterir. |
| [get_LinkSource](./get_linksource/)() const | Bağlı özel belge özelliğinin kaynağını alır. |
| [get_Name](./get_name/)() const | Özelliğin adını döndürür. |
| [get_Type](./get_type/)() const | Özelliğin veri tipini alır. |
| [get_Value](./get_value/)() | Özelliğin değerini alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Ayarlayıcı: [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Özellik değerini bool olarak döndürür. |
| [ToByteArray](./tobytearray/)() | Özellik değerini bayt dizisi olarak döndürür. |
| [ToDateTime](./todatetime/)() | Özellik değerini UTC'de **DateTime** olarak döndürür. |
| [ToDouble](./todouble/)() | Özellik değerini double olarak döndürür. |
| [ToInt](./toint/)() | Özellik değerini integer olarak döndürür. |
| [ToString](./tostring/)() const override | Özellik değerini geçerli yerel ayara göre biçimlendirilmiş bir dize olarak döndürür. |
| static [Type](./type/)() |  |

## Örnekler



Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// \"Document\" nesnesi, meta verilerinin bir kısmını üyelerinde tutar.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Belge ayrıca meta verileri yerleşik özelliklerinde depolar.
// Her yerleşik özellik, belgenin \"BuiltInDocumentProperties\" nesnesinin bir üyesidir.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Bazı özellikler birden fazla değer depolayabilir.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
