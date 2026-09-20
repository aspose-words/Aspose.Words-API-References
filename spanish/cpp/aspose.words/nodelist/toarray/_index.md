---
title: "Método Aspose::Words::NodeList::ToArray"
linktitle: "ToArray"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::NodeList::ToArray. Copia todos los nodos de la colección a una nueva matriz de nodos en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Copia todos los nodos de la colección a una nueva matriz de nodos.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Una matriz de nodos.
## Observaciones


No deberías agregar/eliminar nodos mientras iteras sobre una colección de nodos porque invalida el iterador y requiere actualizaciones para colecciones en vivo.

Para poder agregar/eliminar nodos durante la iteración, usa este método para copiar los nodos a una matriz de tamaño fijo y luego iterar sobre la matriz.

## Ver también

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
