---
title: "Clase Aspose::Words::BookmarkCollection"
linktitle: "BookmarkCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::BookmarkCollection. Una colección de objetos Bookmark que representan los marcadores en el rango especificado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Una colección de objetos [Bookmark](../bookmark/) que representan los marcadores en el rango especificado. Para obtener más información, visite el artículo de documentación [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Elimina todos los marcadores de esta colección y del documento. |
| [get_Count](./get_count/)() | Devuelve el número de marcadores en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve un marcador en el índice especificado. |
| [idx_get](./idx_get/)(const System::String\&) | Devuelve un marcador por nombre. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Elimina el marcador especificado del documento. |
| [Remove](./remove/)(const System::String\&) | Elimina un marcador con el nombre especificado. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un marcador en el índice especificado. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
