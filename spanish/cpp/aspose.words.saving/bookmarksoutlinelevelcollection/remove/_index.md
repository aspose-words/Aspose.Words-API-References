---
title: "Método Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove. Elimina un marcador con el nombre especificado de la colección en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/remove/
---
## BookmarksOutlineLevelCollection::Remove method


Elimina un marcador con el nombre especificado de la colección.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::Remove(const System::String &name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del marcador sin distinción de mayúsculas y minúsculas. |

## Ejemplos



Muestra cómo establecer niveles de esquema para marcadores.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un marcador con otro marcador anidado dentro de él.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Inserta otro marcador.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// Al guardar en .pdf, los marcadores pueden accederse mediante un menú desplegable y usarse como anclas por la mayoría de los lectores.
// Los marcadores también pueden tener valores numéricos para los niveles de esquema,
// permitiendo que las entradas de esquema de nivel inferior oculten las entradas secundarias de nivel superior cuando se colapsan en el lector.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Podemos eliminar dos elementos para que solo quede la designación del nivel de esquema para \"Marcador 1\".
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Hay nueve niveles de esquema. Su numeración se optimizará durante la operación de guardado.
// En este caso, los niveles \"5\" y \"9\" se convertirán en \"2\" y \"3\".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vaciar esta colección preservará los marcadores y los colocará a todos en el mismo nivel de esquema.
outlineLevels->Clear();
```

## Ver también

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
