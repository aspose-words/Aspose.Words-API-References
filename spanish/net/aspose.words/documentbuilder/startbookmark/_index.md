---
title: DocumentBuilder.StartBookmark
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Marca la posición actual en el documento como inicio de marcador.
type: docs
weight: 580
url: /es/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Marca la posición actual en el documento como inicio de marcador.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| bookmarkName | String | Nombre del marcador. |

### Valor_devuelto

El nodo de inicio del marcador que se acaba de crear.

### Observaciones

Los marcadores en un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido necesita llamar a ambos`StartBookmark` y[`EndBookmark`](../endbookmark/) con el mismo **marcadorNombre** parámetro .

Los marcadores mal formados o los marcadores con nombres duplicados se ignorarán cuando se guarde el documento.

### Ejemplos

Muestra cómo crear un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un marcador válido debe tener el texto del cuerpo del documento encerrado entre
// Nodos BookmarkStart y BookmarkEnd creados con un nombre de marcador coincidente.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Inserta un campo de HIPERVÍNCULO que se vincule al marcador. Podemos pasar interruptores de campo
// al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador al que se hace referencia.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ver también

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


