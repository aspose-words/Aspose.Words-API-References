---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.BookmarksOutlineLevelCollection: una poderosa herramienta para administrar marcadores y mejorar la navegación de documentos sin esfuerzo.
type: docs
weight: 5590
url: /es/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Una colección de marcadores individuales a nivel de esquema.

Para obtener más información, visite el[Trabajar con marcadores](https://docs.aspose.com/words/net/working-with-bookmarks/) Artículo de documentación.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Obtiene o establece un nivel de esquema de marcador según el nombre del marcador. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Agrega un marcador a la colección. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Elimina todos los elementos de la colección. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Determina si la colección contiene un marcador con el nombre especificado. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Devuelve el índice basado en cero del marcador especificado en la colección. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Elimina un marcador con el nombre especificado de la colección. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Elimina un marcador en el índice especificado. |

## Observaciones

La clave es un nombre de marcador de cadena que no distingue entre mayúsculas y minúsculas. El valor es un nivel de esquema de marcador de tipo entero.

El nivel de esquema del marcador puede ser un valor de 0 a 9. Especifique 0 y el marcador de Word no se mostrará en el esquema del documento. Especifique 1 y el marcador de Word se mostrará en el esquema del documento en el nivel 1; 2 para el nivel 2 y así sucesivamente.

## Ejemplos

Muestra cómo establecer niveles de esquema para marcadores.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un marcador con otro marcador anidado dentro de él.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Insertar otro marcador.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// Al guardar en formato .pdf, se puede acceder a los marcadores a través de un menú desplegable y la mayoría de los lectores pueden usarlos como anclas.
// Los marcadores también pueden tener valores numéricos para los niveles de esquema,
// permitir que las entradas de esquema de nivel inferior oculten las entradas secundarias de nivel superior cuando se contraen en el lector.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

//Podemos eliminar dos elementos para que solo quede la designación de nivel de esquema para "Marcador 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

Hay nueve niveles de esquema. Su numeración se optimizará al guardar.
// En este caso, los niveles "5" y "9" pasarán a ser "2" y "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vaciar esta colección conservará los marcadores y los colocará todos en el mismo nivel de esquema.
outlineLevels.Clear();
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
