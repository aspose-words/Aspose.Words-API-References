---
title: Enum CommentDisplayMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.CommentDisplayMode enumeración. Especifica el modo de representación de los comentarios del documento.
type: docs
weight: 3290
url: /es/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Especifica el modo de representación de los comentarios del documento.

```csharp
public enum CommentDisplayMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Hide | `0` | No se representan comentarios del documento. |
| ShowInBalloons | `1` | Representa los comentarios del documento en globos en el margen. Este es el valor predeterminado. |
| ShowInAnnotations | `2` | Representa los comentarios del documento en anotaciones. Esto sólo está disponible para formato PDF. |

### Ejemplos

Muestra cómo mostrar comentarios al guardar un documento en un formato renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations solo está disponible en formatos Pdf1.7 y Pdf1.5.
// En otros formatos, funcionará de manera similar a Ocultar.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Tenga en cuenta que es necesario reconstruir el diseño de la página del documento (mediante el método Document.UpdatePageLayout())
// después de cambiar los valores de Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


