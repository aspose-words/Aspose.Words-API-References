---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words para .NET
description: Aspose.Words.Inline clase. Clase base para nodos de nivel en línea que pueden tener formato de caracteres asociado pero que no pueden tener nodos secundarios propios en C#.
type: docs
weight: 3260
url: /es/net/aspose.words/inline/
---
## Inline class

Clase base para nodos de nivel en línea que pueden tener formato de caracteres asociado, pero que no pueden tener nodos secundarios propios.

Para obtener más información, visite el[Niveles lógicos de nodos en un documento](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) artículo de documentación.

```csharp
public abstract class Inline : Node
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devoluciones`verdadero` si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Obtiene el tipo de este nodo. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

Una clase derivada de`Inline` puede ser hijo de[`Paragraph`](../paragraph/).

## Ejemplos

Muestra cómo determinar el tipo de revisión de un nodo en línea.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Cuando editamos el documento mientras la opción "Seguimiento de cambios", que se encuentra en vía Revisar -> Seguimiento,
// está activado en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear las revisiones por
// invocando el método "StartTrackRevisions" del documento y deteniendo el seguimiento utilizando el método "StopTrackRevisions".
// Podemos aceptar revisiones para asimilarlas al documento
// o rechazarlos para cambiar el cambio propuesto de manera efectiva.
Assert.AreEqual(6, doc.Revisions.Count);

// El nodo padre de una revisión es la ejecución a la que se refiere la revisión. Una ejecución es un nodo en línea.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// A continuación se muestran cinco tipos de revisiones que pueden marcar un nodo en línea.
// 1 - Una revisión "insertar":
// Esta revisión ocurre cuando insertamos texto mientras realizamos el seguimiento de los cambios.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Una revisión de "formato":
// Esta revisión ocurre cuando cambiamos el formato del texto mientras realizamos el seguimiento de los cambios.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Una revisión de "paso de":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "mover desde" es una copia del texto original antes de que lo moviéramos.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Una revisión de "mover a":
// La revisión "mover a" es el texto que movimos en su nueva posición en el documento.
// Las revisiones "mover desde" y "mover a" aparecen en pares para cada revisión de movimiento que realizamos.
// Al aceptar una revisión de movimiento se elimina la revisión "mover desde" y su texto,
// y mantiene el texto de la revisión "mover a".
// Al rechazar una revisión de movimiento, se mantiene la revisión de "mover desde" y se elimina la revisión de "mover a".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Una revisión "eliminada":
// Esta revisión ocurre cuando eliminamos texto mientras realizamos un seguimiento de los cambios. Cuando eliminamos texto como este,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// que eliminará el texto definitivamente, o rechazará la revisión, que mantendrá el texto que eliminamos donde estaba.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
