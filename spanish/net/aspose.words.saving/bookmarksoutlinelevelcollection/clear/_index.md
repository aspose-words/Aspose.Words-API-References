---
title: BookmarksOutlineLevelCollection.Clear
second_title: Referencia de API de Aspose.Words para .NET
description: BookmarksOutlineLevelCollection método. Elimina todos los elementos de la colección.
type: docs
weight: 50
url: /es/net/aspose.words.saving/bookmarksoutlinelevelcollection/clear/
---
## BookmarksOutlineLevelCollection.Clear method

Elimina todos los elementos de la colección.

```csharp
public void Clear()
```

### Ejemplos

Muestra cómo establecer niveles de contorno para marcadores.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un marcador con otro marcador anidado dentro.
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

// Al guardar en .pdf, se puede acceder a los marcadores a través de un menú desplegable y la mayoría de los lectores los pueden usar como anclas.
// Los marcadores también pueden tener valores numéricos para niveles de contorno,
// habilitar las entradas de esquema de nivel inferior para ocultar las entradas secundarias de nivel superior cuando se colapsan en el lector.
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

// Podemos eliminar dos elementos para que solo quede la designación de nivel de esquema para "Marcador 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Hay nueve niveles de contorno. Su numeración se optimizará durante la operación de guardado.
// En este caso, los niveles "5" y "9" se convertirán en "2" y "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vaciar esta colección preservará los marcadores y los colocará a todos en el mismo nivel de esquema.
outlineLevels.Clear();
```

### Ver también

* class [BookmarksOutlineLevelCollection](../)
* espacio de nombres [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* asamblea [Aspose.Words](../../../)


