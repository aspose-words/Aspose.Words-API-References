---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection class"
linktitle: "BuildingBlockCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection class. Una colección de objetos BuildingBlock en el documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


Una colección de objetos [BuildingBlock](../buildingblock/) en el documento. Para obtener más información, visite el artículo de documentación del [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un bloque de construcción en el índice especificado. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todos los bloques de construcción de la colección a una nueva matriz de bloques de construcción. |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de esta clase directamente. Para acceder a una colección de bloques de construcción, utilice la propiedad [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## Ver también

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
