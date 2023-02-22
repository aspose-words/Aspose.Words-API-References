---
title: LayoutOptions.CommentDisplayMode
second_title: Referencia de API de Aspose.Words para .NET
description: LayoutOptions propiedad. Obtiene o establece la forma en que se representan los comentarios. El valor predeterminado esShowInBalloons .
type: docs
weight: 30
url: /es/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Obtiene o establece la forma en que se representan los comentarios. El valor predeterminado esShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

### Observaciones

Tenga en cuenta que las revisiones no se representan en globos paraShowInAnnotations .

### Ejemplos

Muestra cómo mostrar comentarios al guardar un documento en un formato renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations solo está disponible en los formatos Pdf1.7 y Pdf1.5.
// En otros formatos, funcionará de manera similar a Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Tenga en cuenta que es necesario reconstruir el diseño de la página del documento (a través del método Document.UpdatePageLayout())
// después de cambiar los valores de Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Ver también

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../layoutoptions/)
* asamblea [Aspose.Words](../../../)


