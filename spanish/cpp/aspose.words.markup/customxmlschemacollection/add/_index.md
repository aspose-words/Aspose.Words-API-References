---
title: "Método Aspose::Words::Markup::CustomXmlSchemaCollection::Add"
linktitle: "Add"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::CustomXmlSchemaCollection::Add. Añade un elemento a la colección en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.markup/customxmlschemacollection/add/
---
## CustomXmlSchemaCollection::Add method


Agrega un elemento a la colección.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::Add(const System::String &value)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | const System::String\& | El elemento a añadir. |

## Ejemplos



Muestra cómo trabajar con una colección de esquemas XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Agregar una asociación de esquema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clona la colección de asociación de esquemas XML de la parte XML personalizada,
// y luego agrega un par de nuevos esquemas al clon.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumere los esquemas e imprima cada elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// A continuación se presentan tres formas de eliminar esquemas de la colección.
// 1 -  Eliminar un esquema por índice:
schemas->RemoveAt(2);

// 2 -  Eliminar un esquema por valor:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Utiliza el método "Clear" para vaciar la colección de una vez.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Ver también

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
