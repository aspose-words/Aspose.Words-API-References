---
title: "Aspose::Words::Properties::DocumentProperty classe"
linktitle: "DocumentProperty"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty classe. Rappresenta una proprietà del documento personalizzata o incorporata. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Rappresenta una proprietà del documento personalizzata o predefinita. Per saperne di più, visita l'articolo di documentazione [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Mostra se questa proprietà è collegata al contenuto o meno. |
| [get_LinkSource](./get_linksource/)() const | Ottiene l'origine di una proprietà del documento personalizzata collegata. |
| [get_Name](./get_name/)() const | Restituisce il nome della proprietà. |
| [get_Type](./get_type/)() const | Ottiene il tipo di dati della proprietà. |
| [get_Value](./get_value/)() | Ottiene o imposta il valore della proprietà. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Setter per [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Restituisce il valore della proprietà come bool. |
| [ToByteArray](./tobytearray/)() | Restituisce il valore della proprietà come array di byte. |
| [ToDateTime](./todatetime/)() | Restituisce il valore della proprietà come **DateTime** in UTC. |
| [ToDouble](./todouble/)() | Restituisce il valore della proprietà come double. |
| [ToInt](./toint/)() | Restituisce il valore della proprietà come intero. |
| [ToString](./tostring/)() const override | Restituisce il valore della proprietà come stringa formattata secondo le impostazioni locali correnti. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
