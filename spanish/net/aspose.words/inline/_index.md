---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Inline, diseñada para el formato de caracteres en nodos en línea. ¡Mejore el estilo de su documento sin nodos secundarios!
type: docs
weight: 3710
url: /es/net/aspose.words/inline/
---
## Inline class

Clase base para nodos de nivel en línea que pueden tener formato de caracteres asociado a ellos, pero no pueden tener nodos secundarios propios.

Para obtener más información, visite el[Niveles lógicos de nodos en un documento](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) Artículo de documentación.

```csharp
public abstract class Inline : Node
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve`verdadero` si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtiene el tipo de este nodo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/)objeto que representa la porción de un documento que está contenida en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

Una clase derivada de`Inline` puede ser un hijo de[`Paragraph`](../paragraph/).

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

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
