---
title: Document.StopTrackRevisions
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Detiene el marcado automático de los cambios del documento como revisiones.
type: docs
weight: 740
url: /es/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Detiene el marcado automático de los cambios del documento como revisiones.

```csharp
public void StopTrackRevisions()
```

### Ejemplos

Muestra cómo realizar un seguimiento de las revisiones mientras se edita un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La edición de un documento generalmente no cuenta como revisión hasta que comenzamos a rastrearlo.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Detener el seguimiento de las revisiones para no contar ninguna edición futura como revisión.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// La creación de revisiones les da una fecha y hora de la operación.
// Podemos desactivar esto pasando DateTime.MinValue cuando comenzamos a realizar el seguimiento de las revisiones.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Podemos aceptar/rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions o el método Accept de cada revisión.
// En Microsoft Word, podemos procesarlos manualmente mediante "Revisar" -> "Cambios".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ver también

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


