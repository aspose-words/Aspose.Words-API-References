---
title: Inline.IsFormatRevision
second_title: Referencia de API de Aspose.Words para .NET
description: Inline propiedad. Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios.
type: docs
weight: 30
url: /es/net/aspose.words/inline/isformatrevision/
---
## Inline.IsFormatRevision property

Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios.

```csharp
public bool IsFormatRevision { get; }
```

### Ejemplos

Muestra cómo determinar el tipo de revisión de un nodo en línea.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Cuando editamos el documento con la opción "Rastrear cambios", que se encuentra en Revisar -> Seguimiento,
// está activado en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones por
// invocando el método "StartTrackRevisions" del documento y deteniendo el seguimiento utilizando el método "StopTrackRevisions".
// Podemos aceptar revisiones para asimilarlas al documento
// o rechazarlos para cambiar el cambio propuesto de manera efectiva.
Assert.AreEqual(6, doc.Revisions.Count);

// El nodo principal de una revisión es la ejecución a la que se refiere la revisión. Una ejecución es un nodo en línea.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// A continuación se muestran cinco tipos de revisiones que pueden marcar un nodo en línea.
// 1 - Una revisión de "insertar":
// Esta revisión ocurre cuando insertamos texto mientras rastreamos cambios.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisión de "formato":
// Esta revisión ocurre cuando cambiamos el formato del texto mientras rastreamos los cambios.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisión de "mover desde":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
// durante el seguimiento de los cambios, aparecen dos revisiones.
// La revisión "mover desde" es una copia del texto original antes de que lo moviéramos.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisión de "mover a":
// La revisión "mover a" es el texto que movimos en su nueva posición en el documento.
// Las revisiones "Mover desde" y "mover a" aparecen en pares para cada revisión de movimiento que llevamos a cabo.
// Aceptar una revisión de movimiento elimina la revisión "mover desde" y su texto,
// y mantiene el texto de la revisión "mover a".
// Por el contrario, rechazar una revisión de movimiento mantiene la revisión "mover desde" y elimina la revisión "mover a".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisión "borrar":
// Esta revisión se produce cuando eliminamos texto durante el seguimiento de los cambios. Cuando eliminamos texto como este,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// que eliminará el texto para siempre, o rechazará la revisión, que mantendrá el texto que eliminamos donde estaba.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ver también

* class [Inline](../)
* espacio de nombres [Aspose.Words](../../inline/)
* asamblea [Aspose.Words](../../../)


