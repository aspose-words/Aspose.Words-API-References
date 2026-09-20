---
title: "Aspose::Words::Bookmark clase"
linktitle: "Marcador"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Bookmark clase. Representa un único marcador. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/bookmark/
---
## Bookmark class


Representa un marcador único. Para obtener más información, visite el artículo de documentación [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Obtiene el nodo que representa el final del marcador. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Obtiene el nodo que representa el inicio del marcador. |
| [get_FirstColumn](./get_firstcolumn/)() | Obtiene el índice basado en cero de la primera columna del rango de columnas de tabla asociado al marcador. |
| [get_IsColumn](./get_iscolumn/)() | Devuelve **true** si este marcador es un marcador de columna de tabla. |
| [get_LastColumn](./get_lastcolumn/)() | Obtiene el índice basado en cero de la última columna del rango de columnas de tabla asociado al marcador. |
| [get_Name](./get_name/)() | Obtiene o establece el nombre del marcador. |
| [get_Text](./get_text/)() | Obtiene el texto contenido en el marcador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina el marcador del documento. No elimina el texto dentro del marcador. |
| [set_Name](./set_name/)(const System::String\&) | Establecedor para [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Establece el texto contenido en el marcador. |
| static [Type](./type/)() |  |
## Observaciones


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
