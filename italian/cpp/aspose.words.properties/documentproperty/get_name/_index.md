---
title: "Aspose::Words::Properties::DocumentProperty::get_Name metodo"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::get_Name metodo. Restituisce il nome della proprietà in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.properties/documentproperty/get_name/
---
## DocumentProperty::get_Name method


Restituisce il nome della proprietà.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_Name() const
```

## Note


Non può essere **null** e non può essere una stringa vuota.

## Esempi



Mostra come lavorare con le proprietà di documento integrate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// L'oggetto "Document" contiene parte dei suoi metadati nei suoi membri.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Il documento memorizza inoltre i metadati nelle sue proprietà integrate.
// Ogni proprietà integrata è un membro dell'oggetto "BuiltInDocumentProperties" del documento.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Alcune proprietà possono contenere più valori.
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

## Vedi anche

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
