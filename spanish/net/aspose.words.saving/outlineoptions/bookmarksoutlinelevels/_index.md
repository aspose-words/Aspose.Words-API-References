---
title: OutlineOptions.BookmarksOutlineLevels
linktitle: BookmarksOutlineLevels
articleTitle: BookmarksOutlineLevels
second_title: Aspose.Words para .NET
description: Descubra la propiedad BookmarksOutlineLevels en OutlineOptions para personalizar la jerarquía de sus marcadores para mejorar la navegación y la experiencia del usuario.
type: docs
weight: 20
url: /es/net/aspose.words.saving/outlineoptions/bookmarksoutlinelevels/
---
## OutlineOptions.BookmarksOutlineLevels property

Permite especificar el nivel de esquema de marcadores individuales.

```csharp
public BookmarksOutlineLevelCollection BookmarksOutlineLevels { get; }
```

## Observaciones

Si no se especifica el nivel de marcador en esta colección, entonces[`DefaultBookmarksOutlineLevel`](../defaultbookmarksoutlinelevel/) Se utiliza el valor.

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

* class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection/)
* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
