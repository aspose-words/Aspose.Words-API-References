---
title: "Metodo Aspose::Words::Properties::DocumentPropertyCollection::idx_get"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Properties::DocumentPropertyCollection::idx_get. Restituisce un oggetto DocumentProperty per indice in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Restituisce un oggetto [DocumentProperty](../../documentproperty/) per indice.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Indice basato su zero del [DocumentProperty](../../documentproperty/) da recuperare. |

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
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Restituisce un oggetto [DocumentProperty](../../documentproperty/) in base al nome della proprietà.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | System::String | Il nome della proprietà da recuperare, senza distinzione tra maiuscole e minuscole. |
## Note


Restituisce **null** se una proprietà con il nome specificato non viene trovata.

## Esempi



Mostra come creare una proprietà documento personalizzata che contiene data e ora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Vedi anche

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
