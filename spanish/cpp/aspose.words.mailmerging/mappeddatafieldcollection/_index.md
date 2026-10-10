---
title: "Clase Aspose::Words::MailMerging::MappedDataFieldCollection"
linktitle: "MappedDataFieldCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::MailMerging::MappedDataFieldCollection. Permite mapear automáticamente entre los nombres de los campos en su fuente de datos y los nombres de los campos de combinación de correspondencia en el documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Permite mapear automáticamente entre los nombres de los campos en su origen de datos y los nombres de los campos de combinación de correspondencia en el documento. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Agrega una nueva asignación de campo. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [ContainsKey](./containskey/)(const System::String\&) | Determina si existe una asignación del campo especificado en el documento dentro de la colección. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Determina si existe una asignación del campo especificado en la fuente de datos dentro de la colección. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador de diccionario que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene o establece el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Obtiene o establece el nombre del campo en la fuente de datos asociado con el campo de combinación de correspondencia especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina una asignación de campo. |
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


Esto se implementa como una colección de claves de cadena a valores de cadena. Las claves son los nombres de los campos de combinación de correspondencia en el documento y los valores son los nombres de los campos en su fuente de datos.

## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
