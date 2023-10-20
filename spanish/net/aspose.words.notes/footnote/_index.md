---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words para .NET
description: Aspose.Words.Notes.Footnote clase. Representa un contenedor para el texto de una nota al pie o nota al final en C#.
type: docs
weight: 4260
url: /es/net/aspose.words.notes/footnote/
---
## Footnote class

Representa un contenedor para el texto de una nota al pie o nota al final.

Para obtener más información, visite el[Trabajar con notas al pie y notas finales](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) artículo de documentación.

```csharp
public class Footnote : InlineStory
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | Inicializa una instancia del`Footnote` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Obtiene el primer párrafo de la historia. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Proporciona acceso al formato de fuente del carácter ancla de este objeto. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Devuelve un valor que especifica si se trata de una nota al pie o al final. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devoluciones`verdadero` si este nodo tiene nodos secundarios. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Contiene un valor que especifica si se trata de una nota al pie numerada automáticamente o una nota al pie con una marca de referencia personalizada definida por el usuario. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devoluciones`verdadero` ya que este nodo puede tener nodos secundarios. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Obtiene el último párrafo de la historia. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | DevolucionesFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Obtiene una colección de párrafos que son hijos inmediatos de la historia. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../../aspose.words/paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Obtiene/establece la marca de referencia personalizada que se utilizará para esta nota al pie. El valor predeterminado es**cuerda vacía** (Empty ), lo que significa que se utilizan notas al pie numeradas automáticamente. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | DevolucionesFootnotes oEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Obtiene una colección de tablas que son hijas inmediatas de la historia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navegador que se puede utilizar para atravesar y leer nodos. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Si el último elemento secundario no es un párrafo, crea y agrega un párrafo vacío. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/)nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selecciona el primero[`Node`](../../aspose.words/node/) que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

El`Footnote` La clase se utiliza para representar notas al pie y notas al final en un documento de Word.

`Footnote` es un nodo de nivel en línea y sólo puede ser hijo de[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` puede contener[`Paragraph`](../../aspose.words/paragraph/) y[`Table`](../../aspose.words.tables/table/) nodos secundarios.

## Ejemplos

Muestra cómo insertar y personalizar notas al pie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega texto y haz referencia a él con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice.
// marque después del texto al que hace referencia y cree una entrada debajo del texto del cuerpo principal en la parte inferior de la página.
// Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
// que pasaremos al método "InsertFootnote" del generador de documentos.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Si esta propiedad se establece en "verdadero", entonces la marca de referencia de nuestra nota al pie
// será su índice entre todas las notas a pie de página de la sección.
// Esta es la primera nota a pie de página, por lo que la marca de referencia será "1".
Assert.True(footnote.IsAuto);

 // Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Podemos establecer una marca de referencia personalizada que usará la nota al pie en lugar de su número de índice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un marcador con el indicador "IsAuto" establecido en verdadero seguirá mostrando su índice real
// incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ver también

* class [InlineStory](../../aspose.words/inlinestory/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
