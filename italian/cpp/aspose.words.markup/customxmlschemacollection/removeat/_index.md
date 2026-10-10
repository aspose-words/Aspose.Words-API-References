---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::RemoveAt metodo"
linktitle: "RemoveAt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::RemoveAt metodo. Rimuove un valore all'indice specificato in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.markup/customxmlschemacollection/removeat/
---
## CustomXmlSchemaCollection::RemoveAt method


Rimuove un valore all'indice specificato.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::RemoveAt(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice a base zero. |

## Esempi



Mostra come lavorare con una raccolta di schemi XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Aggiungi un'associazione di schema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clona la raccolta di associazione di schemi XML della parte XML personalizzata,
// e poi aggiungi un paio di nuovi schemi alla copia.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumera gli schemi e stampa ogni elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Di seguito sono riportati tre modi per rimuovere gli schemi dalla raccolta.
// 1 -  Rimuovi uno schema per indice:
schemas->RemoveAt(2);

// 2 -  Rimuovi uno schema per valore:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Usa il metodo "Clear" per svuotare la collezione in una volta.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Vedi anche

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
