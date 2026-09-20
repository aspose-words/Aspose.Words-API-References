---
title: "Método Aspose::Words::NodeList::idx_get"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeList::idx_get. Recupera un nodo en el índice dado en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Recupera un nodo en el índice dado.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la lista de nodos. |
## Observaciones


El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

## Ver también

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
