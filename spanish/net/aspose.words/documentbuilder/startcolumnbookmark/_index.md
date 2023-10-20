---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words para .NET
description: DocumentBuilder StartColumnBookmark método. Marca la posición actual en el documento como inicio de marcador de columna. La posición debe estar en una celda de la tabla en C#.
type: docs
weight: 620
url: /es/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Marca la posición actual en el documento como inicio de marcador de columna. La posición debe estar en una celda de la tabla.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| bookmarkName | String | Nombre del marcador. |

### Valor_devuelto

El nodo de inicio del marcador que se acaba de crear.

## Observaciones

Un marcador de columna cubre una o más columnas en un rango de filas. Para crear un marcador válido, you necesita llamar a ambos`StartColumnBookmark` y[`EndColumnBookmark`](../endcolumnbookmark/) con el mismo *bookmarkName*parámetro.

Los marcadores mal formados o con nombres duplicados se ignorarán cuando se guarde el documento.

La posición real del insertado.[`BookmarkStart`](../../bookmarkstart/) El nodo puede diferir de la posición actual del constructor document .

## Ejemplos

Muestra cómo crear un marcador de columna.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Las celdas 1,2,4,5 se marcarán como favoritas.
builder.StartColumnBookmark("MyBookmark_1");
// Los marcadores mal formados o con nombres duplicados se ignorarán cuando se guarde el documento.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### Ver también

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
