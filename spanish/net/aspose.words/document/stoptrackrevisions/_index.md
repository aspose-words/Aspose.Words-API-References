---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words para .NET
description: Aprenda a utilizar el método StopTrackRevisions para evitar las marcas de cambios automáticos en los documentos, mejorando así la eficiencia de la edición y la claridad del documento.
type: docs
weight: 770
url: /es/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Detiene el marcado automático de cambios en el documento como revisiones.

```csharp
public void StopTrackRevisions()
```

## Ejemplos

Muestra cómo realizar un seguimiento de las revisiones mientras se edita un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editar un documento generalmente no cuenta como una revisión hasta que comenzamos a realizar un seguimiento.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

//Dejar de rastrear revisiones para no contar ninguna edición futura como revisión.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

//La creación de revisiones les da una fecha y hora de la operación.
//Podemos deshabilitar esto pasando DateTime.MinValue cuando comenzamos a rastrear revisiones.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

//Podemos aceptar o rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions, o el método Accept de cada revisión.
// En Microsoft Word, podemos procesarlos manualmente a través de "Revisar" -> "Cambios".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Ver también

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
