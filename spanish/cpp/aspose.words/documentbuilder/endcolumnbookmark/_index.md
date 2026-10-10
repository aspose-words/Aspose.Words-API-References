---
title: "Método Aspose::Words::DocumentBuilder::EndColumnBookmark"
linktitle: "EndColumnBookmark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::EndColumnBookmark. Marca la posición actual en el documento como el final de un marcador de columna. La posición debe estar en una celda de tabla en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


Marca la posición actual en el documento como el final de un marcador de columna. La posición debe estar en una celda de tabla.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nombre del marcador. |

### ReturnValue

El nodo de fin de marcador que acaba de crearse.
## Observaciones


Un marcador de columna abarca una o más columnas en un rango de filas. Para crear un marcador válido necesitas llamar tanto a [StartColumnBookmark()](../) como a [EndColumnBookmark()](../) con el mismo parámetro *bookmarkName*.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

La posición real del nodo [BookmarkEnd](../../bookmarkend/) insertado puede diferir de la posición actual del document builder.

## Ejemplos



Muestra cómo crear un marcador de columna.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Se marcarán las celdas 1,2,4,5.
builder->StartColumnBookmark(u"MyBookmark_1");
// Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## Ver también

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
