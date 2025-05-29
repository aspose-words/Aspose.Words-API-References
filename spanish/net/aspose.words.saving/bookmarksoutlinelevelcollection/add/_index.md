---
title: BookmarksOutlineLevelCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Descubra cómo mejorar su proyecto con el método BookmarksOutlineLevelCollection Add, agregando sin esfuerzo marcadores a su colección para una mejor organización.
type: docs
weight: 40
url: /es/net/aspose.words.saving/bookmarksoutlinelevelcollection/add/
---
## BookmarksOutlineLevelCollection.Add method

Agrega un marcador a la colección.

```csharp
public void Add(string name, int outlineLevel)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre del marcador que se agregará, que no distingue entre mayúsculas y minúsculas. |
| outlineLevel | Int32 | Nivel de contorno del marcador. El rango válido es de 0 a 9. |

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

* class [BookmarksOutlineLevelCollection](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
