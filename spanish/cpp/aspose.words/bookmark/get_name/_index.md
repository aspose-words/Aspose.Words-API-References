---
title: "Aspose::Words::Bookmark::get_Name method"
linktitle: "get_Name"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Bookmark::get_Name method. Obtiene o establece el nombre del marcador en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Obtiene o establece el nombre del marcador.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Ejemplos



Muestra cómo insertar un marcador.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un marcador válido tiene un nombre, un nodo BookmarkStart y un nodo BookmarkEnd.
// Cualquier espacio en blanco en los nombres de los marcadores se convertirá en guiones bajos si abrimos el documento guardado con Microsoft Word.
// Si resaltamos el nombre del marcador en Microsoft Word mediante Insertar -> Enlaces -> Marcador, y pulsamos "Ir a",
// el cursor saltará al texto encerrado entre los nodos BookmarkStart y BookmarkEnd.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Los marcadores se almacenan en esta colección.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Ver también

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
