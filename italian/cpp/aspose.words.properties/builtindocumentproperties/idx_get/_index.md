---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get metodo. Restituisce un oggetto DocumentProperty in base al nome della proprietà in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Restituisce un oggetto [DocumentProperty](../../documentproperty/) in base al nome della proprietà.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | System::String | Il nome della proprietà da recuperare, senza distinzione tra maiuscole e minuscole. |
## Note


I nomi stringa delle proprietà corrispondono ai nomi delle proprietà tipizzate disponibili da [BuiltInDocumentProperties](../).

Se richiedi una proprietà che non è presente nel documento, ma il nome della proprietà è riconosciuto come un nome incorporato valido, viene creata una nuova [DocumentProperty](../../documentproperty/), aggiunta alla collezione e restituita. Alla proprietà appena creata viene assegnato un valore predefinito (stringa vuota, zero, **false** o DateTime.MinValue a seconda del tipo della proprietà incorporata).

Se richiedi una proprietà che non è presente nel documento e il nome non è riconosciuto come un nome incorporato, viene restituito **null**.

## Esempi



Mostra come lavorare con le proprietà personalizzate del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate, che, come le proprietà integrate, sono coppie chiave-valore.
// Il documento ha un elenco fisso di proprietà integrate. L'utente crea tutte le proprietà personalizzate.
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

## Vedi anche

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
