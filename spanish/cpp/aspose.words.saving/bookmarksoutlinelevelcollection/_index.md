---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection clase"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection clase. Una colección del nivel de esquema de marcadores individuales. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


Una colección del nivel de esquema de marcadores individuales. Para obtener más información, visite el artículo de documentación [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Agrega un marcador a la colección. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [Contains](./contains/)(const System::String\&) | Determina si la colección contiene un marcador con el nombre dado. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene o establece el nivel de esquema del marcador por el nombre del marcador. |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece el nivel de esquema del marcador en el índice especificado. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Obtiene o establece el nivel de esquema del marcador por el nombre del marcador. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Obtiene o establece el nivel de esquema del marcador en el índice especificado. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Devuelve el índice basado en cero del marcador especificado en la colección. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina un marcador con el nombre especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un marcador en el índice especificado. |
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


La clave es un nombre de marcador de cadena que no distingue entre mayúsculas y minúsculas. El valor es un int nivel de esquema de marcador.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
