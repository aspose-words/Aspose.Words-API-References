---
title: StartTrackRevisions
second_title: Referencia de API de Aspose.Words para .NET
description: Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión.
type: docs
weight: 690
url: /es/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y la hora que se usarán para las revisiones. |

### Observaciones

Si llama a este método y luego realiza algunos cambios en el documento mediante programación, guarde el documento y luego abra el documento en MS Word, verá estos cambios como revisiones.

Actualmente, Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

Se admite el seguimiento automático de cambios tanto al modificar este documento a través del nodo manipulaciones como al usar[`DocumentBuilder`](../../documentbuilder/)

Este método no cambia la[`TrackRevisions`](../trackrevisions/) opción y no utiliza su valor con fines de seguimiento de revisión.

### Ejemplos

Muestra cómo realizar un seguimiento de las revisiones mientras se edita un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La edición de un documento generalmente no cuenta como una revisión hasta que comenzamos a rastrearlos.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Detener el seguimiento de las revisiones para no contar las ediciones futuras como revisiones.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Crear revisiones les da una fecha y hora de la operación.
// Podemos deshabilitar esto pasando DateTime.MinValue cuando empecemos a rastrear las revisiones.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Podemos aceptar/rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions, o al método Accept de cada revisión.
// En Microsoft Word, podemos procesarlos manualmente a través de "Revisar" -> "Cambios".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ver también

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión.

```csharp
public void StartTrackRevisions(string author)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| author | String | Iniciales del autor a utilizar para las revisiones. |

### Observaciones

Si llama a este método y luego realiza algunos cambios en el documento mediante programación, guarde el documento y luego abra el documento en MS Word, verá estos cambios como revisiones.

Actualmente, Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

Se admite el seguimiento automático de cambios tanto al modificar este documento a través del nodo manipulaciones como al usar[`DocumentBuilder`](../../documentbuilder/)

Este método no cambia la[`TrackRevisions`](../trackrevisions/) opción y no utiliza su valor con fines de seguimiento de revisión.

### Ejemplos

Muestra cómo realizar un seguimiento de las revisiones mientras se edita un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La edición de un documento generalmente no cuenta como una revisión hasta que comenzamos a rastrearlos.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Detener el seguimiento de las revisiones para no contar las ediciones futuras como revisiones.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Crear revisiones les da una fecha y hora de la operación.
// Podemos deshabilitar esto pasando DateTime.MinValue cuando empecemos a rastrear las revisiones.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Podemos aceptar/rechazar estas revisiones programáticamente
// llamando a métodos como Document.AcceptAllRevisions, o al método Accept de cada revisión.
// En Microsoft Word, podemos procesarlos manualmente a través de "Revisar" -> "Cambios".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ver también

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
