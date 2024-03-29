---
title: Paragraph.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words para .NET
description: Paragraph IsDeleteRevision propiedad. Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C#.
type: docs
weight: 40
url: /es/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsDeleteRevision { get; }
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

// Los párrafos anteriores no son revisiones.
// Los párrafos que agreguemos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Insertar".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Los párrafos que eliminemos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Eliminar".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Dichos párrafos permanecerán hasta que aceptemos o rechacemos la revisión eliminada.
// Aceptar la revisión eliminará el párrafo para siempre,
// y rechazar la revisión la dejará en el documento como si nunca la hubiéramos eliminado.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Acepte la revisión y luego verifique que el párrafo haya desaparecido.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
