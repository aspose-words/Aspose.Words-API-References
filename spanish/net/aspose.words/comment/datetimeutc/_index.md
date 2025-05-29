---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words para .NET
description: Descubra la propiedad Comment DateTimeUtc, que recupera la fecha y hora UTC exactas de sus comentarios para un seguimiento y una gestión precisos.
type: docs
weight: 50
url: /es/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Obtiene la fecha y hora UTC en que se realizó el comentario.

```csharp
public DateTime DateTimeUtc { get; }
```

## Observaciones

El valor predeterminado es MinValue

## Ejemplos

Muestra cómo obtener la fecha y hora UTC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

DateTime dateTime = DateTime.Now;
Comment comment = new Comment(doc, "John Doe", "J.D.", dateTime);
comment.SetText("My comment.");

builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.UtcDateTime.docx");
doc = new Document(ArtifactsDir + "Comment.UtcDateTime.docx");

comment = (Comment)doc.GetChild(NodeType.Comment, 0, true);
// DateTimeUtc devuelve datos sin milisegundos.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Ver también

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
