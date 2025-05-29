---
title: Inline.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words para .NET
description: Descubra la propiedad Inline ParentParagraph para acceder fácilmente al párrafo padre de cualquier nodo, mejorando la estructura y la eficiencia de su codificación.
type: docs
weight: 70
url: /es/net/aspose.words/inline/parentparagraph/
---
## Inline.ParentParagraph property

Recupera el padre[`Paragraph`](../../paragraph/) de este nodo.

```csharp
public Paragraph ParentParagraph { get; }
```

## Ejemplos

Muestra cómo determinar el tipo de revisión de un nodo en línea.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Cuando editamos el documento mientras está activa la opción "Seguimiento de cambios", que se encuentra en Vía Revisión -> Seguimiento,
// está activado en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear las revisiones
// invocar el método "StartTrackRevisions" del documento y detener el seguimiento utilizando el método "StopTrackRevisions".
//Podemos aceptar revisiones para asimilarlas al documento.
// o rechazarlos para cambiar efectivamente el cambio propuesto.
Assert.AreEqual(6, doc.Revisions.Count);

El nodo padre de una revisión es la ejecución a la que se refiere. Una ejecución es un nodo en línea.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// A continuación se muestran cinco tipos de revisiones que pueden marcar un nodo en línea.
// 1 - Una revisión "insertar":
//Esta revisión ocurre cuando insertamos texto mientras hacemos un seguimiento de los cambios.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisión de "formato":
//Esta revisión ocurre cuando cambiamos el formato del texto mientras hacemos un seguimiento de los cambios.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisión de "movimiento desde":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "mover desde" es una copia del texto original antes de que lo moviéramos.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisión "pasar a":
// La revisión "mover a" es el texto que movimos a su nueva posición en el documento.
// Las revisiones "Mover desde" y "mover a" aparecen en pares para cada revisión de movimiento que realizamos.
// Al aceptar una revisión de movimiento se elimina la revisión "mover desde" y su texto,
// y conserva el texto de la revisión "mover a".
// Rechazar una revisión de movimiento, por el contrario, conserva la revisión "mover desde" y elimina la revisión "mover a".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisión "eliminada":
Esta revisión ocurre cuando eliminamos texto durante el seguimiento de cambios. Al eliminar texto de esta manera,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// lo que eliminará el texto para siempre, o rechazará la revisión, lo que mantendrá el texto que eliminamos donde estaba.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ver también

* class [Paragraph](../../paragraph/)
* class [Inline](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
