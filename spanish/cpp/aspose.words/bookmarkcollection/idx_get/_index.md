---
title: "Método Aspose::Words::BookmarkCollection::idx_get"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BookmarkCollection::idx_get. Devuelve un marcador por nombre en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


Devuelve un marcador por nombre.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nombre del marcador sin distinción entre mayúsculas y minúsculas. |
## Observaciones


Devuelve **null** si no se puede encontrar el marcador con el nombre especificado.

## Ver también

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Devuelve un marcador en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la colección. |
## Observaciones


El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

## Ver también

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
