---
title: InlineStory.IsMoveToRevision
second_title: Referencia de API de Aspose.Words para .NET
description: InlineStory propiedad. Devoluciones verdadero si este objeto se movió insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.
type: docs
weight: 60
url: /es/net/aspose.words/inlinestory/ismovetorevision/
---
## InlineStory.IsMoveToRevision property

Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsMoveToRevision { get; }
```

### Ejemplos

Muestra cómo ver las propiedades relacionadas con la revisión de los nodos de InlineStory.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Cuando editamos el documento con la opción "Rastrear cambios", que se encuentra en Revisar -> Seguimiento,
// está activado en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones por
// invocando el método "StartTrackRevisions" del documento y deteniendo el seguimiento utilizando el método "StopTrackRevisions".
// Podemos aceptar revisiones para asimilarlas al documento
// o rechazarlos para deshacer y descartar el cambio propuesto.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// A continuación se muestran cinco tipos de revisiones que pueden marcar un nodo InlineStory.
// 1 - Una revisión de "insertar":
// Esta revisión ocurre cuando insertamos texto mientras rastreamos cambios.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Una revisión de "mover desde":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
// durante el seguimiento de los cambios, aparecen dos revisiones.
// La revisión "mover desde" es una copia del texto original antes de que lo moviéramos.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Una revisión de "mover a":
// La revisión "mover a" es el texto que movimos en su nueva posición en el documento.
// Las revisiones "Mover desde" y "mover a" aparecen en pares para cada revisión de movimiento que llevamos a cabo.
// Aceptar una revisión de movimiento elimina la revisión "mover desde" y su texto,
// y mantiene el texto de la revisión "mover a".
// Por el contrario, rechazar una revisión de movimiento mantiene la revisión "mover desde" y elimina la revisión "mover a".
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Una revisión de "borrar":
// Esta revisión se produce cuando eliminamos texto durante el seguimiento de los cambios. Cuando eliminamos texto como este,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// que eliminará el texto para siempre, o rechazará la revisión, que mantendrá el texto que eliminamos donde estaba.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Ver también

* class [InlineStory](../)
* espacio de nombres [Aspose.Words](../../inlinestory/)
* asamblea [Aspose.Words](../../../)


