---
title: RevisionCollection Class
linktitle: RevisionCollection
articleTitle: RevisionCollection
second_title: Aspose.Words para .NET
description: Aspose.Words.RevisionCollection clase. Una colección deRevision objetos que representan revisiones en el documento en C#.
type: docs
weight: 4770
url: /es/net/aspose.words/revisioncollection/
---
## RevisionCollection class

Una colección de[`Revision`](../revision/) objetos que representan revisiones en el documento.

Para obtener más información, visite el[Seguimiento de cambios en un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) artículo de documentación.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | Devuelve el número de revisiones de la colección. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | Colección de grupos de revisión. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | Devuelve un[`Revision`](../revision/) en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | Acepta todas las revisiones de esta colección. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | Rechaza todas las revisiones de esta colección. |

## Observaciones

No crea instancias de esta clase directamente. Utilizar el[`Revisions`](../document/revisions/) propiedad para obtener revisiones presentes en un documento.

## Ejemplos

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

* class [Revision](../revision/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
