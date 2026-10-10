---
title: "Aspose::Words::Properties::CustomDocumentProperties class"
linktitle: "CustomDocumentProperties"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::CustomDocumentProperties class. Una raccolta di proprietà personalizzate del documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Una raccolta di proprietà del documento personalizzate. Per saperne di più, visita l'articolo di documentazione [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Crea una nuova proprietà personalizzata del documento di tipo dati [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Crea una nuova proprietà personalizzata del documento di tipo dati [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Crea una nuova proprietà personalizzata del documento di tipo dati [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Crea una nuova proprietà personalizzata del documento di tipo dati [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Crea una nuova proprietà personalizzata del documento di tipo dati [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Crea una nuova proprietà personalizzata del documento collegata al contenuto. |
| [Clear](../documentpropertycollection/clear/)() | Rimuove tutte le proprietà dalla raccolta. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Restituisce **true** se una proprietà con il nome specificato esiste nella raccolta. |
| [get_Count](../documentpropertycollection/get_count/)() | Ottiene il numero di elementi nella raccolta. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Restituisce un oggetto [DocumentProperty](../documentproperty/) per nome della proprietà. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Restituisce un oggetto [DocumentProperty](../documentproperty/) per indice. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Ottiene l'indice di una proprietà per nome. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Rimuove una proprietà all'indice specificato. |
| static [Type](./type/)() |  |
## Note


Ogni oggetto [DocumentProperty](../documentproperty/) rappresenta una proprietà personalizzata di un documento contenitore.

I nomi delle proprietà non distinguono tra maiuscole e minuscole.

Le proprietà nella raccolta sono ordinate alfabeticamente per nome.

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
