---
title: "Clase Aspose::Words::Markup::CustomXmlSchemaCollection"
linktitle: "CustomXmlSchemaCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Markup::CustomXmlSchemaCollection. Una colección de cadenas que representan esquemas XML asociados a una parte XML personalizada. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


Una colección de cadenas que representan esquemas XML asociados a una parte XML personalizada. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&) | Agrega un elemento a la colección. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [Clone](./clone/)() | Crea una clonación profunda de este objeto. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece el elemento en el índice especificado. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtiene o establece el elemento en el índice especificado. |
| [IndexOf](./indexof/)(const System::String\&) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina el valor especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un valor en el índice especificado. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Observaciones


No crea instancias de esta clase. Accede a la colección de esquemas XML de una parte XML personalizada a través de la propiedad [Schemas](../customxmlpart/get_schemas/).

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
