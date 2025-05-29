---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsInsertRevision del párrafo en Word. Aprenda cómo identifica el texto insertado durante el seguimiento de cambios para una gestión eficiente de documentos.
type: docs
weight: 110
url: /es/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsInsertRevision { get; }
```

## Ejemplos

Muestra cómo trabajar con párrafos de revisión.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

//Los párrafos anteriores no son revisiones.
// Los párrafos que agreguemos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Insertar".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Los párrafos que eliminemos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Eliminar".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

//Estos párrafos permanecerán hasta que aceptemos o rechacemos la revisión de eliminación.
// Al aceptar la revisión se eliminará el párrafo definitivamente.
// y rechazar la revisión la dejará en el documento como si nunca la hubiéramos eliminado.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Acepte la revisión y luego verifique que el párrafo haya desaparecido.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
