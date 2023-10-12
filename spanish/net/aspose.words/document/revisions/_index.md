---
title: Document.Revisions
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene una colección de revisiones cambios rastreados que existen en este documento.
type: docs
weight: 350
url: /es/net/aspose.words/document/revisions/
---
## Document.Revisions property

Obtiene una colección de revisiones (cambios rastreados) que existen en este documento.

```csharp
public RevisionCollection Revisions { get; }
```

### Observaciones

La colección devuelta es una colección "activa", lo que significa que si elimina partes de un documento que contiene revisiones, las revisiones eliminadas desaparecerán automáticamente de esta colección.

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

// Esta bandera corresponde a la "Revisión" -> "Seguimiento" -> Opción "Seguimiento de cambios" en Microsoft Word.
// El método "StartTrackRevisions" no afecta su valor,
// y el documento realiza un seguimiento de las revisiones mediante programación a pesar de tener un valor de "falso".
// Si abrimos este documento usando Microsoft Word, no realizará un seguimiento de las revisiones.
Assert.IsFalse(doc.TrackRevisions);

// Hemos agregado texto usando el generador de documentos, por lo que la primera revisión es una revisión de tipo inserción.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Eliminar una ejecución para crear una revisión de tipo eliminación.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Agregar una nueva revisión la coloca al comienzo de la colección de revisiones.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Las revisiones de inserción aparecen en el cuerpo del documento incluso antes de que aceptemos/rechacemos la revisión.
// Rechazar la revisión eliminará sus nodos del cuerpo. Por el contrario, los nodos que componen eliminan revisiones.
// también permanece en el documento hasta que aceptemos la revisión.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Al aceptar la revisión eliminada se eliminará su nodo principal del texto del párrafo
// y luego eliminar la revisión de la colección.
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

* class [RevisionCollection](../../revisioncollection/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


