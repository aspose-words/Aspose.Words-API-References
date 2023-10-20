---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words para .NET
description: DocumentBuilder EndBookmark método. Marca la posición actual en el documento como final del marcador en C#.
type: docs
weight: 210
url: /es/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Marca la posición actual en el documento como final del marcador.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| bookmarkName | String | Nombre del marcador. |

### Valor_devuelto

El nodo final del marcador que se acaba de crear.

## Observaciones

Los marcadores de un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido necesita llamar a ambos[`StartBookmark`](../startbookmark/) y`EndBookmark` con el mismo*bookmarkName* parámetro.

Los marcadores mal formados o con nombres duplicados se ignorarán cuando se guarde el documento.

## Ejemplos

Muestra cómo crear un marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un marcador válido debe tener el texto del cuerpo del documento encerrado por
// Nodos BookmarkStart y BookmarkEnd creados con un nombre de marcador coincidente.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Muestra cómo insertar un hipervínculo que haga referencia a un marcador local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Inserta un campo HIPERVÍNCULO que enlace al marcador. Podemos pasar interruptores de campo.
// al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador al que se hace referencia.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ver también

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
