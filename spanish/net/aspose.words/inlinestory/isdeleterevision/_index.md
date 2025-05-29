---
title: InlineStory.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad IsDeleteRevision de InlineStory mejora su experiencia en Microsoft Word al rastrear los cambios eliminados sin esfuerzo.
type: docs
weight: 30
url: /es/net/aspose.words/inlinestory/isdeleterevision/
---
## InlineStory.IsDeleteRevision property

Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsDeleteRevision { get; }
```

## Ejemplos

Muestra cómo ver las propiedades relacionadas con la revisión de los nodos InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Cuando editamos el documento mientras está activa la opción "Seguimiento de cambios", que se encuentra en Vía Revisión -> Seguimiento,
// está activado en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear las revisiones
// invocar el método "StartTrackRevisions" del documento y detener el seguimiento utilizando el método "StopTrackRevisions".
//Podemos aceptar revisiones para asimilarlas al documento.
// o rechazarlos para deshacer y descartar el cambio propuesto.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// A continuación se muestran cinco tipos de revisiones que pueden marcar un nodo InlineStory.
// 1 - Una revisión "insertar":
//Esta revisión ocurre cuando insertamos texto mientras hacemos un seguimiento de los cambios.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Una revisión de "movimiento desde":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "mover desde" es una copia del texto original antes de que lo moviéramos.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Una revisión "mover a":
// La revisión "mover a" es el texto que movimos a su nueva posición en el documento.
// Las revisiones "Mover desde" y "mover a" aparecen en pares para cada revisión de movimiento que realizamos.
// Al aceptar una revisión de movimiento se elimina la revisión "mover desde" y su texto,
// y conserva el texto de la revisión "mover a".
// Rechazar una revisión de movimiento, por el contrario, conserva la revisión "mover desde" y elimina la revisión "mover a".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Una revisión "eliminada":
Esta revisión ocurre cuando eliminamos texto durante el seguimiento de cambios. Al eliminar texto de esta manera,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// lo que eliminará el texto para siempre, o rechazará la revisión, lo que mantendrá el texto que eliminamos donde estaba.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Ver también

* class [InlineStory](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
