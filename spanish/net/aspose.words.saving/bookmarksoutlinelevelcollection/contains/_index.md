---
title: BookmarksOutlineLevelCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words para .NET
description: BookmarksOutlineLevelCollection Contains método. Determina si la colección contiene un marcador con el nombre de pila en C#.
type: docs
weight: 60
url: /es/net/aspose.words.saving/bookmarksoutlinelevelcollection/contains/
---
## BookmarksOutlineLevelCollection.Contains method

Determina si la colección contiene un marcador con el nombre de pila.

```csharp
public bool Contains(string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | Nombre del marcador que se va a localizar sin distinguir entre mayúsculas y minúsculas. |

### Valor_devuelto

`verdadero` si el artículo se encuentra en la colección; de lo contrario,`FALSO`.

## Ejemplos

Muestra cómo establecer niveles de contorno para marcadores.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un marcador con otro marcador anidado en su interior.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Inserta otro marcador.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// Al guardar en .pdf, se puede acceder a los marcadores a través de un menú desplegable y la mayoría de los lectores pueden utilizarlos como anclas.
// Los marcadores también pueden tener valores numéricos para los niveles de esquema,
// habilitando entradas de esquema de nivel inferior para ocultar entradas secundarias de nivel superior cuando se contraen en el lector.
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

// Podemos eliminar dos elementos para que solo quede la designación del nivel de esquema para "Marcador 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Hay nueve niveles de esquema. Su numeración se optimizará durante la operación de guardar.
// En este caso, los niveles "5" y "9" pasarán a ser "2" y "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Al vaciar esta colección se conservarán los marcadores y se colocarán todos en el mismo nivel de esquema.
outlineLevels.Clear();
```

### Ver también

* class [BookmarksOutlineLevelCollection](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
