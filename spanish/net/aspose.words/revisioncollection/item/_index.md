---
title: RevisionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda fácilmente a revisiones específicas con la propiedad Elemento RevisionCollection. Recupere rápidamente revisiones por índice para una gestión de datos optimizada.
type: docs
weight: 30
url: /es/net/aspose.words/revisioncollection/item/
---
## RevisionCollection indexer

Devuelve un[`Revision`](../../revision/) en el índice especificado.

```csharp
public Revision this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice de la colección. |

## Observaciones

El índice está basado en cero.

Se permiten índices negativos e indican acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos de la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que la cantidad de elementos de la lista, esto devuelve una referencia nula.

## Ejemplos

Muestra cómo trabajar con revisiones en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//La edición normal del documento no cuenta como una revisión.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Para registrar nuestras ediciones como revisiones, necesitamos declarar un autor y luego comenzar a rastrearlas.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Esta bandera corresponde a la opción "Revisar" -> "Seguimiento" -> "Control de cambios" en Microsoft Word.
// El método "StartTrackRevisions" no afecta su valor,
// y el documento está rastreando revisiones programáticamente a pesar de tener un valor de "falso".
// Si abrimos este documento con Microsoft Word, no se realizará un seguimiento de las revisiones.
Assert.IsFalse(doc.TrackRevisions);

//Hemos agregado texto usando el generador de documentos, por lo que la primera revisión es una revisión de tipo inserción.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

//Elimina una ejecución para crear una revisión de tipo eliminación.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Agregar una nueva revisión la coloca al comienzo de la colección de revisiones.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Las revisiones insertadas aparecen en el cuerpo del documento incluso antes de que aceptemos o rechacemos la revisión.
Rechazar la revisión eliminará sus nodos del cuerpo. Por el contrario, los nodos que conforman la revisión eliminan las revisiones.
// también permanecerá en el documento hasta que aceptemos la revisión.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Al aceptar la revisión de eliminación se eliminará su nodo principal del texto del párrafo.
// y luego eliminar la revisión de la colección en sí.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Ahora mueva el nodo para crear un tipo de revisión en movimiento.
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

* class [Revision](../../revision/)
* class [RevisionCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
