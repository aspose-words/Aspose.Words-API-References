---
title: DocumentBuilder.StartBookmark
linktitle: StartBookmark
articleTitle: StartBookmark
second_title: Aspose.Words para .NET
description: Utilice el método StartBookmark de DocumentBuilder para marcar y administrar fácilmente posiciones clave en su documento, mejorando la organización y la navegación.
type: docs
weight: 650
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

## Observaciones

Los marcadores de un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido, es necesario llamar a ambos.`StartBookmark` y[`EndBookmark`](../endbookmark/) con el mismo*bookmarkName* Parámetro .

Los marcadores mal formados o con nombres duplicados se ignorarán cuando se guarde el documento.

## Ejemplos

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

// Insertar un campo HIPERVÍNCULO que enlaza al marcador. Podemos pasar modificadores de campo.
// al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador referenciado.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ver también

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
