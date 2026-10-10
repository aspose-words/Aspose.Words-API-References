---
title: "Aspose::Words::Properties::DocumentProperty::get_Value metodu"
linktitle: "get_Value"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentProperty::get_Value metodu. C++'ta özelliğin değerini alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


Özelliğin değerini alır veya ayarlar.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## Açıklamalar


**null** olamaz.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
