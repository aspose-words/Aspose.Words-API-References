---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words para .NET
description: Document StartTrackRevisions método. Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión en C#.
type: docs
weight: 710
url: /es/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| author | String | Iniciales del autor a utilizar en las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |

## Observaciones

Si llama a este método y luego realiza algunos cambios en el documento mediante programación, guarda el documento y luego lo abre en MS Word, verá estos cambios como revisiones.

Actualmente, Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

Se admite el seguimiento automático de cambios tanto al modificar este documento mediante manipulaciones de nodo como al utilizar[`DocumentBuilder`](../../documentbuilder/)

Este método no cambia la[`TrackRevisions`](../trackrevisions/) opción y no utiliza su value para fines de seguimiento de revisiones.

## Ejemplos

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión.

```csharp
public void StartTrackRevisions(string author)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| author | String | Iniciales del autor a utilizar en las revisiones. |

## Observaciones

Si llama a este método y luego realiza algunos cambios en el documento mediante programación, guarda el documento y luego lo abre en MS Word, verá estos cambios como revisiones.

Actualmente, Aspose.Words solo admite el seguimiento de inserciones y eliminaciones de nodos. Los cambios de formato no se registran como revisiones.

Se admite el seguimiento automático de cambios tanto al modificar este documento mediante manipulaciones de nodo como al utilizar[`DocumentBuilder`](../../documentbuilder/)

Este método no cambia la[`TrackRevisions`](../trackrevisions/) opción y no utiliza su value para fines de seguimiento de revisiones.

## Ejemplos

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
