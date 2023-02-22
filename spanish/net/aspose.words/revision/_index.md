---
title: Class Revision
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Revision clase. Representa una revisión cambio registrado en un estilo o nodo de documento. UsarRevisionType para comprobar el tipo de esta revisión.
type: docs
weight: 4500
url: /es/net/aspose.words/revision/
---
## Revision class

Representa una revisión (cambio registrado) en un estilo o nodo de documento. Usar[`RevisionType`](./revisiontype/) para comprobar el tipo de esta revisión.

```csharp
public class Revision
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Obtiene o establece el autor de esta revisión. No puede ser una cadena vacía o nula. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Obtiene o establece la fecha/hora de esta revisión. |
| [Group](../../aspose.words/revision/group/) { get; } | Obtiene el grupo de revisión. Devuelve nulo si la revisión no pertenece a ningún grupo. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Obtiene el nodo principal inmediato (propietario) de esta revisión. Esta propiedad funcionará para cualquier tipo de revisión que no seaStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Obtiene el estilo primario inmediato (propietario) de esta revisión. Esta propiedad funcionará solo para elStyleDefinitionChange tipo de revisión. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Obtiene el tipo de esta revisión. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Acepta esta revisión. |
| [Reject](../../aspose.words/revision/reject/)() | Rechazar esta revisión. |

### Ejemplos

Muestra cómo trabajar con revisiones en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La edición normal del documento no cuenta como revisión.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Para registrar nuestras ediciones como revisiones, debemos declarar un autor y luego comenzar a rastrearlas.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Esta bandera corresponde a la "Revisión" -> "Seguimiento" -> Opción "Control de cambios" en Microsoft Word.
// El método "StartTrackRevisions" no afecta su valor,
// y el documento realiza un seguimiento de las revisiones mediante programación a pesar de tener un valor de "falso".
// Si abrimos este documento usando Microsoft Word, no estará rastreando las revisiones.
Assert.IsFalse(doc.TrackRevisions);

// Hemos agregado texto utilizando el generador de documentos, por lo que la primera revisión es una revisión de tipo inserción.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Eliminar una ejecución para crear una revisión de tipo eliminación.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Agregar una nueva revisión la coloca al principio de la colección de revisiones.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Las revisiones de inserción aparecen en el cuerpo del documento incluso antes de que aceptemos/rechacemos la revisión.
// Rechazar la revisión eliminará sus nodos del cuerpo. Por el contrario, los nodos que componen eliminar revisiones
// también permanecen en el documento hasta que aceptemos la revisión.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Aceptar la revisión de eliminación eliminará su nodo principal del texto del párrafo
// y luego elimine la revisión de la colección en sí.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Ahora mueva el nodo para crear un tipo de revisión móvil.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// La revisión en movimiento ahora está en el índice 1. Rechace la revisión para descartar su contenido.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


