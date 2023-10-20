---
title: BookmarksOutlineLevelCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: BookmarksOutlineLevelCollection Item propiedad. Obtiene o establece un nivel de esquema de marcador por el nombre del marcador en C#.
type: docs
weight: 30
url: /es/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Obtiene o establece un nivel de esquema de marcador por el nombre del marcador.

```csharp
public int this[string name] { get; set; }
```

| Parámetro | Descripción |
| --- | --- |
| name | Nombre del marcador que no distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

El nivel de esquema del marcador. El rango válido es de 0 a 9.

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

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Obtiene o establece un nivel de esquema de marcador en el índice especificado.

```csharp
public int this[int index] { get; set; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Índice de base cero del marcador. |

### Valor_devuelto

El nivel de esquema del marcador. El rango válido es de 0 a 9.

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
